---
title: Retail Modern POS (MPOS) トランザクション ページへのカスタム コントロールの追加
description: このトピックでは、画面レイアウト デザイナーを使用して トランザクション ページに新しいカスタム コントロールを追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 24411
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-11-22
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 241eac07f54d84a1b8cad931215126f3cd9f9779
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023457"
---
# <a name="add-custom-controls-to-retail-modern-pos-mpos-transaction-pages"></a><span data-ttu-id="5877d-103">Retail Modern POS (MPOS) トランザクション ページへのカスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="5877d-103">Add custom controls to Retail Modern POS (MPOS) transaction pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5877d-104">カスタム コントロールを使用して、トランザクション ページにさらに情報を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="5877d-104">You can add more information to a transaction page by using custom controls.</span></span> <span data-ttu-id="5877d-105">画面レイアウト デザイナーを使用して、トランザクション ページにカスタム コントロールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="5877d-105">You can add a custom control to a transaction page by using the screen layout designer.</span></span> <span data-ttu-id="5877d-106">デザイナーで、ドラッグ アンド ドロップ操作を使用してカスタム コントロールを追加してから、コントロールの位置、高さ、および幅を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5877d-106">In the designer, you can use a drag-and-drop operation to add the custom control, and then set the location, height, and width of the control.</span></span> <span data-ttu-id="5877d-107">POS 拡張フレームワークを使用して、独自の拡張機能にカスタム コントロール用ビジネス ロジックを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="5877d-107">You can implement business logic for the custom control in your own extensions by using the POS extension framework.</span></span> <span data-ttu-id="5877d-108">このトピックでは、選択した行の項目、項目 ID、および説明の詳細を示す新しいカスタム コントロールを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5877d-108">This topic explains how to add a new custom control that shows the details for the selected line item, the item ID, and the description.</span></span>

> [!NOTE]
> <span data-ttu-id="5877d-109">このトピックでは Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 Retail プラットフォーム更新 8 と Retail アプリ更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="5877d-109">This topic applies to Dynamics 365 for Finance and Operations, and to Microsoft Dynamics 365 Retail with platform update 8 and Retail App update 4 hotfix.</span></span>

## <a name="add-a-new-custom-control"></a><span data-ttu-id="5877d-110">新しいカスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="5877d-110">Add a new custom control</span></span>

1. <span data-ttu-id="5877d-111">Dynamics 365 Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="5877d-111">Sign in to Dynamics 365 Retail.</span></span>
2. <span data-ttu-id="5877d-112">**Retail** > **チャネル設定** > **POS 設定** > **POS** > **画面レイアウト**と選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-112">Select **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>
3. <span data-ttu-id="5877d-113">**F3MGR** 画面レイアウト ID を選択した後、アクション ウィンドウで **デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-113">Select the **F3MGR** screen layout ID, and then, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="5877d-114">レイアウト サイズとして **1440 x 960: フル レイアウト** を選択し、**レイアウト デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-114">Select **1440x960 – Full layout** as the layout size, and then select **Layout designer**.</span></span>
5. <span data-ttu-id="5877d-115">デザイナー ツールをインストールするように求められたら、**開く** を選択し、インストール手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5877d-115">If you're prompted to install the designer tool, select **Open**, and follow the installation instructions.</span></span>
6. <span data-ttu-id="5877d-116">Azure Active Directory (Azure AD) の資格情報の入力を要求するメッセージが表示されたら、その情報を入力してデザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="5877d-116">When you're prompted for your Microsoft Azure Active Directory (Azure AD) credentials, enter the information to start the designer.</span></span>
7. <span data-ttu-id="5877d-117">デザイナーで、カスタム コントロールを左ウィンドウからページにドラッグして、必要に応じてカスタム コントロールを調整、サイズ変更、または位置変更します。</span><span class="sxs-lookup"><span data-stu-id="5877d-117">In the designer, drag the custom control from the left pane to the page, and then adjust, resize, or reposition the custom control as you require.</span></span>
8. <span data-ttu-id="5877d-118">ページで、カスタム コントロールを右クリックし、**カスタマイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-118">On the page, right-click the custom control, and then select **Customize**.</span></span>
9. <span data-ttu-id="5877d-119">ダイアログ ボックスで、これらのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5877d-119">In the dialog box, set these properties:</span></span>

   - <span data-ttu-id="5877d-120">**コントロール名:** lineDetails</span><span class="sxs-lookup"><span data-stu-id="5877d-120">**Control Name:** lineDetails</span></span>
   - <span data-ttu-id="5877d-121">**パッケージ名:** Pos_Extensibility_Samples</span><span class="sxs-lookup"><span data-stu-id="5877d-121">**Package Name:** Pos_Extensibility_Samples</span></span>
   - <span data-ttu-id="5877d-122">**パブリッシャー名:** Contoso</span><span class="sxs-lookup"><span data-stu-id="5877d-122">**Publisher Name:** Contoso</span></span>

     > [!NOTE]
     > <span data-ttu-id="5877d-123">これらの名前は、拡張子マニフェスト内の名前と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5877d-123">These names should match the names in the extension manifest.</span></span>

10. <span data-ttu-id="5877d-124">**閉じる**ボタン (**X**) を選択し、デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5877d-124">Close the designer by selecting the **Close** button (**X**).</span></span>
11. <span data-ttu-id="5877d-125">変更の保存を求められたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-125">When you're prompted to save your changes, select **Yes**.</span></span> <span data-ttu-id="5877d-126">**いいえ**を選択した場合、変更は保存されません。</span><span class="sxs-lookup"><span data-stu-id="5877d-126">If you select **No**, your changes won't be saved.</span></span>
12. <span data-ttu-id="5877d-127">**小売** > **小売 IT** > **配送スケジュール** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-127">Select **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
13. <span data-ttu-id="5877d-128">**1090 レジスター** ジョブを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-128">Select the **Registers (1090)** job, and then select **Run now**.</span></span>

## <a name="add-business-logic-to-the-custom-control"></a><span data-ttu-id="5877d-129">カスタム コントロールへのビジネス ロジックの追加</span><span class="sxs-lookup"><span data-stu-id="5877d-129">Add business logic to the custom control</span></span>

1. <span data-ttu-id="5877d-130">Microsoft Visual Studio 2015 を管理者として起動します。</span><span class="sxs-lookup"><span data-stu-id="5877d-130">Start Microsoft Visual Studio 2015 as an administrator.</span></span>
2. <span data-ttu-id="5877d-131">**ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="5877d-131">Open the **ModernPOS** solution from **…\RetailSDK\POS**.</span></span>
3. <span data-ttu-id="5877d-132">**POS.Extensions** プロジェクトで、**CustomControlExtensions** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="5877d-132">In the **POS.Extensions** project, create a folder that is named **CustomControlExtensions**.</span></span>
4. <span data-ttu-id="5877d-133">**CustomControlExtensions** フォルダーで、**Cart** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="5877d-133">In the **CustomControlExtensions** folder, create a folder that is named **Cart**.</span></span>
5. <span data-ttu-id="5877d-134">**カート** フォルダーで、**CartViewController.ts** という Typescript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5877d-134">In the **Cart** folder, create a Typescript file that is named **CartViewController.ts**.</span></span>
6. <span data-ttu-id="5877d-135">**CartViewController.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="5877d-135">In the **CartViewController.ts** file, add the following **import** statement to import the relevant entities and context.</span></span>

    ```typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { IExtensionCartViewControllerContext } from "PosApi/Extend/Views/CartView";
    import * as CartView from "PosApi/Extend/Views/CartView";
    ```

7. <span data-ttu-id="5877d-136">**CartViewController** という名前のクラスを作成し、**CartExtensionViewControllerBase** からクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5877d-136">Create a class that is named **CartViewController**, and extend it from **CartExtensionViewControllerBase**.</span></span> <span data-ttu-id="5877d-137">**CartExtensionViewControllerBase** クラスには、買い物カゴおよび支払/入金の明細行、カートの明細行の選択ハンドラー、買い物カゴの明細行がクリアされたハンドラーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5877d-137">The **CartExtensionViewControllerBase** class contains the cart and tender lines, the cart line selected handler, and the cart line cleared handler.</span></span> <span data-ttu-id="5877d-138">これらの要素は、カスタム コントロールで選択した行を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5877d-138">These elements will be used to show the selected line in the custom control.</span></span>

    ```typescript
    export default class CartViewController extends CartView.CartExtensionViewControllerBase {

    }
    ```

8. <span data-ttu-id="5877d-139">**CartViewController** クラスで、選択したカート明細行および支払/入金明細行を取得する 2 つのプライベート変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="5877d-139">In the **CartViewController** class, add two private variables to get the selected cart lines and tender lines.</span></span>

    ```typescript
    private _selectedCartLines: ProxyEntities.CartLine[];

    private _selectedTenderLines: ProxyEntities.TenderLine[];
    ```

9. <span data-ttu-id="5877d-140">カートと入金の選択情報を設定するクラス **コンストラクター** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="5877d-140">Create a class **constructor** method to set the cart and tender selection information.</span></span>

    ```typescript
    constructor(context: IExtensionCartViewControllerContext) {
        super(context);
        this.cartLineSelectedHandler = (data: CartView.CartLineSelectedData): void => {
            this._selectedCartLines = data.cartLines;
        };

        this.cartLineSelectionClearedHandler = (): void => {
            this._selectedCartLines = undefined;
        };

        this.tenderLineSelectedHandler = (data: CartView.TenderLineSelectedData): void => {
            this._selectedTenderLines = data.tenderLines;
        };

        this.tenderLineSelectionClearedHandler = (): void => {
            this._selectedCartLines = undefined;
        };
    }
    ```

    <span data-ttu-id="5877d-141">全体的なクラスは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5877d-141">The overall class should look like this.</span></span>

    ```typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { IExtensionCartViewControllerContext } from "PosApi/Extend/Views/CartView";
    import * as CartView from "PosApi/Extend/Views/CartView";

    export default class CartViewController extends CartView.CartExtensionViewControllerBase {
        private _selectedCartLines: ProxyEntities.CartLine[];
        private _selectedTenderLines: ProxyEntities.TenderLine[];

        /**
        * Creates a new instance of the CartViewController class.
        * @param {IExtensionCartViewControllerContext} context The events Handler context.
        * @remarks The events handler context contains APIs through which a handler can communicate with POS.
        */
        constructor(context: IExtensionCartViewControllerContext) {
            super(context);
            this.cartLineSelectedHandler = (data: CartView.CartLineSelectedData): void => {
                this._selectedCartLines = data.cartLines;
            };

            this.cartLineSelectionClearedHandler = (): void => {
                this._selectedCartLines = undefined;
            };

            this.tenderLineSelectedHandler = (data: CartView.TenderLineSelectedData): void => {
                this._selectedTenderLines = data.tenderLines;
            };

            this.tenderLineSelectionClearedHandler = (): void => {
                this._selectedCartLines = undefined;
            };
        }
    }
    ```

10. <span data-ttu-id="5877d-142">**カート** フォルダーで、**LineDetailsCustomControl.html** という HTML ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5877d-142">In the **Cart** folder, create an HTML file that is named **LineDetailsCustomControl.html**.</span></span>
11. <span data-ttu-id="5877d-143">**LineDetailsCustomControl.html** ファイルで、選択した明細行項目の ID と説明を表示する 2 つのテキスト フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="5877d-143">In the **LineDetailsCustomControl.html** file, add two text fields to show the ID and description for the selected line item.</span></span> <span data-ttu-id="5877d-144">既定のコードを削除し、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5877d-144">Delete the default code, and add the following code.</span></span>

    ```typescript
    <!DOCTYPE html>
        <html lang="en" xmlns="http://www.w3.org/1999/xhtml">
            <head>
                <meta charset="utf-8" />
                <title></title>
            </head>
            <body>
                <!-- Note: The element ID differs from the ID generated by the POS extensibility framework. This 'template' ID is not used by the POS extensibility framework. -->
                <script id="Microsoft_Pos_Extensibility_Samples_LineDetails" type="text/html">
                    <!-- ko ifnot: isCartLineSelected -->
                    <h4>No cart lines selected</h4>
                    <!-- /ko -->
                    <!-- ko if: isCartLineSelected -->
                    <h4 data-bind="text: cartLineItemId">Item ID</h4>
                    <h4 data-bind="text: cartLineDescription">Item ID</h4>
                    <!-- /ko -->;
                </script>
            </body>
        </html>
        ```

12. In the **Cart** folder, create a Typescript file that is named **LineDetailsCustomControl.ts**.
13. In the **LineDetailsCustomControl.ts** file, add the logic to bind the line details information.
14. Import the POS entities and type extensions to use the reference type in the constructor and other events.

    ```typescript
    import {
        ObjectExtensions,
        StringExtensions,
        ArrayExtensions
    } from "PosApi/TypeExtensions";
    import { ProxyEntities } from "PosApi/Entities";
    ```

15. <span data-ttu-id="5877d-145">クラスを作成し、**CartViewCustomControlBase** からクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5877d-145">Create a class, and extend it from **CartViewCustomControlBase**.</span></span>

    ```typescript
    export default class LineDetailsCustomControl extends CartViewCustomControlBase {}
    ```

16. <span data-ttu-id="5877d-146">次のプライベート変数を宣言し、買い物カゴの品目 ID と説明を設定します。</span><span class="sxs-lookup"><span data-stu-id="5877d-146">Declare the following private variables to set the cart item ID and description.</span></span>

    ```typescript
    private static readonly TEMPLATE_ID: string = "Microsoft_Pos_Extensibility_Samples_LineDetails";
    public readonly cartLineItemId: Computed<string>;
    public readonly cartLineDescription: Computed<string>;
    public readonly isCartLineSelected: Computed<boolean>;
    private readonly _cartLine: Observable<ProxyEntities.CartLine>;
    private _state: ICartViewCustomControlState;
    ```

17. <span data-ttu-id="5877d-147">**コンストラクター** メソッドを作成して、選択したハンドラーを初期化して取得します。</span><span class="sxs-lookup"><span data-stu-id="5877d-147">Create the **constructor** method to initialize and get the selected handler.</span></span>

    ```typescript
    constructor(id: string, context: ICartViewCustomControlContext) {
        super(id, context);
        this._cartLine = ko.observable(null);
        this.cartLineItemId = ko.computed(() => {
            let cartLine: ProxyEntities.CartLine = this._cartLine();
            if (!ObjectExtensions.isNullOrUndefined(cartLine)) {
                return cartLine.ItemId;
            }
            return StringExtensions.EMPTY;
        });

        this.cartLineDescription = ko.computed(() => {
            let cartLine: ProxyEntities.CartLine = this._cartLine();
            if (!ObjectExtensions.isNullOrUndefined(cartLine)) {
                return cartLine.Description;
            }
            return StringExtensions.EMPTY;
        });

        this.isCartLineSelected = ko.computed(() =>; !ObjectExtensions.isNullOrUndefined(this._cartLine()));
        this.cartLineSelectedHandler = (data: CartLineSelectedData) => {
            if (ArrayExtensions.hasElements(data.cartLines)) {
                this._cartLine(data.cartLines[0]);
            }
        };

        this.cartLineSelectionClearedHandler = () => {
            this._cartLine(null);
        };
    }
    ```

18. <span data-ttu-id="5877d-148">**onReady** メソッドを追加して、コントロールを指定した HTML 要素にバインドします。</span><span class="sxs-lookup"><span data-stu-id="5877d-148">Add the **onReady** method to bind the control to the specified HTML element.</span></span>

    ```typescript
    public onReady(element: HTMLElement): void {
        ko.applyBindingsToNode(element, {
            template: {
                name: LineDetailsCustomControl.TEMPLATE_ID,
                data: this
            }
        });
    }
    ```

19. <span data-ttu-id="5877d-149">**init** メソッドを追加して状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="5877d-149">Add the **init** method to set the state.</span></span>

    ```typescript
    public init(state: ICartViewCustomControlState): void {
        this._state = state;
    }
    ```

    <span data-ttu-id="5877d-150">全体的なクラスは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5877d-150">The overall class should look like this.</span></span>

    ```typescript
    import {
        CartViewCustomControlBase,
        ICartViewCustomControlState,
        ICartViewCustomControlContext,
        CartLineSelectedData
        } from "PosApi/Extend/Views/CartView";

    import {
        ObjectExtensions,
        StringExtensions,
        ArrayExtensions
    } from "PosApi/TypeExtensions";

    import { ProxyEntities } from "PosApi/Entities";

    export default class LineDetailsCustomControl extends CartViewCustomControlBase {
        private static readonly TEMPLATE_ID: string = "Microsoft_Pos_Extensibility_Samples_LineDetails";
        public readonly cartLineItemId: Computed<string>;
        public readonly cartLineDescription: Computed<string>;
        public readonly isCartLineSelected: Computed<boolean>;
        private readonly_cartLine: Observable<ProxyEntities.CartLine>;
        private _state: ICartViewCustomControlState;

        constructor(id: string, context: ICartViewCustomControlContext) {
            super(id, context);
            this._cartLine = ko.observable(null);

            this.cartLineItemId = ko.computed(() => {
                let cartLine: ProxyEntities.CartLine = this._cartLine();
                if (!ObjectExtensions.isNullOrUndefined(cartLine)) {
                    return cartLine.ItemId;
                }
                return StringExtensions.EMPTY;
            });

            this.cartLineDescription = ko.computed(() => {
                let cartLine: ProxyEntities.CartLine = this._cartLine();
                if (!ObjectExtensions.isNullOrUndefined(cartLine)) {
                    return cartLine.Description;
                }
                return StringExtensions.EMPTY;
            });

            this.isCartLineSelected = ko.computed(() => !ObjectExtensions.isNullOrUndefined(this._cartLine()));
            this.cartLineSelectedHandler = (data: CartLineSelectedData) => {
                if (ArrayExtensions.hasElements(data.cartLines)) {
                    this._cartLine(data.cartLines[0]);
                }
            };

            this.cartLineSelectionClearedHandler = () => {
                this._cartLine(null);
            };
        }

        /**
        * Binds the control to the specified element.
        * @param {HTMLElement} element The element to which the control should be bound.
        */
        public onReady(element: HTMLElement): void {
            ko.applyBindingsToNode(element, {
                template: {
                    name: LineDetailsCustomControl.TEMPLATE_ID,
                    data: this
                }
            });
        }

        /**
        * Initializes the control.
        * @param {ICartViewCustomControlState} state The initial state of the page used to initialize the control.
        */
        public init(state: ICartViewCustomControlState): void {
            this._state = state;
        }
    }
    ```

20. <span data-ttu-id="5877d-151">**CustomControlExtensions** フォルダーで、**manifest.json** という JSON ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5877d-151">In the **CustomControlExtensions** folder, create a JSON file that is named **manifest.json**.</span></span>
21. <span data-ttu-id="5877d-152">**manifest.json** ファイルに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5877d-152">In the **manifest.json** file, add the following code.</span></span>

    ```typescript
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_Samples",
        "publisher": "Contoso",
        "version": "7.2.0",
        "minimumPosVersion": "7.2.0.0",
        "components": {
            "extend": {
                "views": {
                    "CartView": {
                        "viewController": { "modulePath": "Cart/CartViewController" },
                        "controlsConfig": {
                            "customControls": [
                            {
                                "controlName": "lineDetails",
                                "htmlPath": "Cart/LineDetailsCustomControl.html",
                                "modulePath": "Cart/LineDetailsCustomControl"
                            }
                            ]
                        }
                    }
                }
            }
        } 
    }
    ```

22. <span data-ttu-id="5877d-153">**POS.Extensions** プロジェクトで **extensions.json** ファイルを開き、次の **CustomControlExtensions** サンプルで更新して、POS が実行時にこの拡張機能に含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="5877d-153">In the **POS.Extensions** project, open the **extensions.json** file, and update it with the following **CustomControlExtensions** samples, so that the POS includes this extension at runtime.</span></span>

    ```typescript
    {
        "extensionPackages": [
        {
            "baseUrl": "SampleExtensions2"
        },
        {
            "baseUrl": "CustomControlExtensions"
        }
        ]
    }
    ```

23. <span data-ttu-id="5877d-154">**tsconfig.json** ファイルで、除外リストに拡張パッケージ フォルダーをコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="5877d-154">In the **tsconfig.json** file, comment out the extension package folders in the exclude list.</span></span> <span data-ttu-id="5877d-155">POS は、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="5877d-155">The POS uses this file to include or exclude the extension.</span></span> <span data-ttu-id="5877d-156">既定では、リストに除外された拡張リスト全体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5877d-156">By default, the list contains the whole excluded extensions list.</span></span> <span data-ttu-id="5877d-157">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、除外リストの拡張子をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="5877d-157">To include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the exclude list, as shown here.</span></span>

    ```typescript
    "exclude": [
        "SampleExtensions"
        //"SampleExtensions2",
        //"CustomControlExtensions"
    ],
    ```

24. <span data-ttu-id="5877d-158">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="5877d-158">Compile and rebuild the project.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="5877d-159">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="5877d-159">Validate the customization</span></span>

1. <span data-ttu-id="5877d-160">オペレーター ID に **000160**、パスワードに **123** を使用して Retail Modern POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="5877d-160">Sign in to Retail Modern POS by using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="5877d-161">**ようこそ**画面で、**現在のトランザクション**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-161">On the **Welcome** screen, select the **Current transaction** button.</span></span>
3. <span data-ttu-id="5877d-162">トランザクションを任意の品目に追加し、追加した明細行品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="5877d-162">Add any item to the transaction, and then select the line item that you added.</span></span>

    <span data-ttu-id="5877d-163">カスタム コントロールには、選択した明細行品目の ID と説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5877d-163">The custom control should show the ID and description for the selected line item.</span></span>
