---
title: カスタム ボタンを POS ヘッダー バーに追加
description: このトピックでは、POS ヘッダー バーに新しいカスタム ボタンを追加する方法について説明します。
author: mugunthanm
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 09-16-2020
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: c68efaac430d937d0085f899dcbd23f93d118642
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792989"
---
# <a name="add-custom-buttons-to-the-pos-header-bar"></a><span data-ttu-id="f4db3-103">カスタム ボタンを POS ヘッダー バーに追加</span><span class="sxs-lookup"><span data-stu-id="f4db3-103">Add custom buttons to the POS header bar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4db3-104">このトピックでは、販売時点管理 (POS) ヘッダー バーに新しいカスタム ボタンを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-104">This topic explains how to add a new custom button to the header bar in the point of sale (POS).</span></span> <span data-ttu-id="f4db3-105">POS ヘッダー バー拡張機能は、Microsoft Dynamics 365 Commerce バージョン 10.0.14 以降でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f4db3-105">The POS header bar extension is supported by Microsoft Dynamics 365 Commerce version 10.0.14 and later.</span></span>

<span data-ttu-id="f4db3-106">カスタム ヘッダー ボタンには、コントロール ユーザー インターフェイス (UI)、スタイル、およびテーマを説明するカスケード スタイル シート (CSS) コードを含む HTML ファイルが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4db3-106">The custom header button must contain an HTML file that includes Cascading Style Sheets (CSS) code that describes the control user interface (UI), styles, and themes.</span></span> <span data-ttu-id="f4db3-107">また、ロジックを指定する TypeScript ビュー モデル ファイルも含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4db3-107">It must also contain a TypeScript view model file that specifies the logic.</span></span> <span data-ttu-id="f4db3-108">ファイル ビュー モデル ファイル内のクラスは、ヘッダー ボタンのプロパティおよびイベントを継承するために、**CustomPackingItem** クラスを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4db3-108">The class inside the file view model file must extend the **CustomPackingItem** class, so that it inherits the header button properties and events.</span></span> <span data-ttu-id="f4db3-109">**cartChangedHandler** イベントは、カート内で何らかの変更があった場合に通知を行うために、ヘッダー ボタンで公開されています。</span><span class="sxs-lookup"><span data-stu-id="f4db3-109">The **cartChangedHandler** event is exposed on the header button to provide notification if something changes in the cart.</span></span> <span data-ttu-id="f4db3-110">拡張コードは、カート イベントに基づくカスタム ロジックを実行することも、カスタム ビジネス ロジックを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-110">Your extension code can do custom logic that is based on cart events, or it can do custom business logic.</span></span>

## <a name="custompackingitem-class"></a><span data-ttu-id="f4db3-111">CustomPackingItem クラス</span><span class="sxs-lookup"><span data-stu-id="f4db3-111">CustomPackingItem class</span></span>

### <a name="properties"></a><span data-ttu-id="f4db3-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4db3-112">Properties</span></span>

| <span data-ttu-id="f4db3-113">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4db3-113">Property</span></span> | <span data-ttu-id="f4db3-114">説明</span><span class="sxs-lookup"><span data-stu-id="f4db3-114">Description</span></span> |
|----------|-------------|
| <span data-ttu-id="f4db3-115">CustomPackingItemPosition</span><span class="sxs-lookup"><span data-stu-id="f4db3-115">CustomPackingItemPosition</span></span> | <span data-ttu-id="f4db3-116">POS ヘッダー品目に対する品目の位置。</span><span class="sxs-lookup"><span data-stu-id="f4db3-116">The item's position relative to the POS header items.</span></span> |
| <span data-ttu-id="f4db3-117">ICustomPackingItemContext</span><span class="sxs-lookup"><span data-stu-id="f4db3-117">ICustomPackingItemContext</span></span> | <span data-ttu-id="f4db3-118">カスタム ヘッダー梱包品目のコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="f4db3-118">The context of the custom header packing item.</span></span> |

### <a name="events-and-methods"></a><span data-ttu-id="f4db3-119">イベントおよびメソッド</span><span class="sxs-lookup"><span data-stu-id="f4db3-119">Events and methods</span></span>

| <span data-ttu-id="f4db3-120">イベントまたはメソッド</span><span class="sxs-lookup"><span data-stu-id="f4db3-120">Event or method</span></span> | <span data-ttu-id="f4db3-121">説明</span><span class="sxs-lookup"><span data-stu-id="f4db3-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="f4db3-122">cartChangedHandler</span><span class="sxs-lookup"><span data-stu-id="f4db3-122">cartChangedHandler</span></span> | <span data-ttu-id="f4db3-123">**CartUpdated** イベントのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="f4db3-123">The handler for the **CartUpdated** event.</span></span> |
| <span data-ttu-id="f4db3-124">コンストラクター (ID: 文字列、コンテキスト: ICustomPackingItemContext)</span><span class="sxs-lookup"><span data-stu-id="f4db3-124">constructor(id: string, context: ICustomPackingItemContext)</span></span> | <span data-ttu-id="f4db3-125">このメソッドは、**CustomHeaderPackingItem** クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-125">This method creates a new instance of the **CustomHeaderPackingItem** class.</span></span> |
| <span data-ttu-id="f4db3-126">ID()</span><span class="sxs-lookup"><span data-stu-id="f4db3-126">id()</span></span> | <span data-ttu-id="f4db3-127">このメソッドは、カスタム ヘッダー梱包品目の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-127">This method gets the identifier of the custom header packing item.</span></span> |
| <span data-ttu-id="f4db3-128">表示の取得 (): ブール値</span><span class="sxs-lookup"><span data-stu-id="f4db3-128">get visible(): boolean</span></span> | <span data-ttu-id="f4db3-129">このメソッドは、表示される値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-129">This method gets the visible value.</span></span> |
| <span data-ttu-id="f4db3-130">表示設定 (isVisible: ブール値)</span><span class="sxs-lookup"><span data-stu-id="f4db3-130">set visible(isVisible: boolean)</span></span> | <span data-ttu-id="f4db3-131">このメソッドは、表示される値を設定します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-131">This method sets the visible value.</span></span> |
| <span data-ttu-id="f4db3-132">抽象 onReady (packedElement: HTMLElement、unpackedElement: HTMLElement): 無効</span><span class="sxs-lookup"><span data-stu-id="f4db3-132">abstract onReady(packedElement: HTMLElement, unpackedElement: HTMLElement): void</span></span> | <span data-ttu-id="f4db3-133">このメソッドは、コントロール要素の準備ができたら、呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-133">This method is called when the control element is ready.</span></span> |
| <span data-ttu-id="f4db3-134">処分 (): 無効</span><span class="sxs-lookup"><span data-stu-id="f4db3-134">dispose(): void</span></span> | <span data-ttu-id="f4db3-135">このメソッドは、コントロールを破棄してリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-135">This method disposes of the control and releases its resources.</span></span> |
| <span data-ttu-id="f4db3-136">保護された抽象 init (状態: ICustomPackingItemState): 無効</span><span class="sxs-lookup"><span data-stu-id="f4db3-136">protected abstract init(state: ICustomPackingItemState): void</span></span> | <span data-ttu-id="f4db3-137">このメソッドは、コントロールを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-137">This method initializes the control.</span></span> |

<span data-ttu-id="f4db3-138">次の例に示すように、**manifest.json** ファイルにヘッダー ボタン拡張機能のノードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4db3-138">You must add nodes for the header button extension in the **manifest.json** file, as shown in the following example.</span></span>

```typescript
"header": {
    "customPackingItems": [
        {
            "name": " name of the control",
            "description": "Description.",
            "modulePath": " view model file name with path",
            "htmlPath": " html file name with path"
        }
    ]
}
```

## <a name="add-a-custom-button-to-the-pos-header-bar"></a><span data-ttu-id="f4db3-139">カスタム ボタンを POS ヘッダー バーに追加</span><span class="sxs-lookup"><span data-stu-id="f4db3-139">Add a custom button to the POS header bar</span></span>

<span data-ttu-id="f4db3-140">次の手順に従って、ヘッダー バーにカスタム ボタンを追加し、請求額をカートから読み取って表示します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-140">Follow these steps to add a custom button to the header bar and show the amount due by reading it from the cart.</span></span>

1. <span data-ttu-id="f4db3-141">Visual Studio 2017 を開きます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-141">Open Visual Studio 2017.</span></span>
2. <span data-ttu-id="f4db3-142">**\\RetailSDK\\POS** から **ModernPOS/CloudPOS** ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-142">Open the **ModernPOS/CloudPOS** solution from **\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="f4db3-143">**POS.Extensions** プロジェクトで、**HeaderExtensionSample** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-143">In the **POS.Extensions** project, create a folder that is named **HeaderExtensionSample**.</span></span>
4. <span data-ttu-id="f4db3-144">**HeaderExtensionSample** フォルダーで、**CartAmountDuePackingItem.html** という HTML ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-144">In the **HeaderExtensionSample** folder, create an HTML file that is named **CartAmountDuePackingItem.html**.</span></span>
5. <span data-ttu-id="f4db3-145">次のコードをコピーして、ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-145">Copy the following code, and paste it into the file.</span></span>

    ```html
    <!DOCTYPE html>
    <html lang="en" xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Cart Amount Due Item Templates</title>
    </head>
    <body>
        <script id="Microsoft_Pos_Extensibility_Samples_UnpackedCartAmountDueItem" type="text/html">
            <button class="pad0 center row"
                    data-bind="click: onItemClickedHandler">
                <div class="iconShop buttonIcon height20"></div>
                <div class="h4 padRight8" data-bind="text: amountDueLabel"></div>
            </button>
        </script>
        <script id="Microsoft_Pos_Extensibility_Samples_PackedCartAmountDueItem" type="text/html">
            <button class="row pad0"
                    data-bind="click: onItemClickedHandler">
                <div class="iconShop buttonIcon height20 margin12">
                </div>
                <div class="grow row marginLeft8 padTop12">
                    <div class="h4 padRight4">Amount due: </div>
                    <div class="h4 padRight8" data-bind="text: amountDueLabel"></div>
                </div>
            </button>
        </script>
    </body>
    </html>
    ```

6. <span data-ttu-id="f4db3-146">**HeaderExtensionSample** フォルダーで、**CartAmountDuePackingItem.ts** という TypeScript ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-146">In the **HeaderExtensionSample** folder, create a TypeScript file that is named **CartAmountDuePackingItem.ts**.</span></span>
7. <span data-ttu-id="f4db3-147">次のコードをコピーして、ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-147">Copy the following code, and paste it into the file.</span></span>

    ```typescript
    import {
        CustomPackingItem, ICustomPackingItemContext, CustomPackingItemPosition, ICustomPackingItemState, CartChangedData
    } from "PosApi/Extend/Header";
    import { CurrencyFormatter } from "PosApi/Consume/Formatters";
    import { ClientEntities } from "PosApi/Entities";
    import { StringExtensions } from "PosApi/TypeExtensions";

    /**
     * (Sample) Custom packing item that shows the cart's amount due and navigates to the cart on click.
     */
    export default class CartAmountDuePackingItem extends CustomPackingItem {
        /**
         * The position of the custom packing item relative to the out-of-the-box items.
         */
        public readonly position: CustomPackingItemPosition = CustomPackingItemPosition.After;

        /**
         * Label displayed in the custom packing item with the current amount due.
         */
        public amountDueLabel: Observable<string>;

        private _currentAmountDue: Observable<number>;
        private _amountDueSubscription: IDisposable;

        /**
         * Initializes a new instance of the CartAmountDuePackingItem class.
         * @param {string} id The item identifier.
         * @param {ICustomPackingItemContext} context The custom packing item context.
         */
        constructor(id: string, context: ICustomPackingItemContext) {
            super(id, context);

            this.amountDueLabel = ko.observable(StringExtensions.EMPTY);

            this._currentAmountDue = ko.observable(0);
            this._amountDueSubscription = this._currentAmountDue.subscribe((newValue: number) => {
                if (newValue > 0) {
                    this.amountDueLabel(CurrencyFormatter.toCurrency(newValue));
                    this.visible = true;
                } else {
                    this.visible = false;
                }
            });

            this.cartChangedHandler = this._cartChangedHandler.bind(this);
        }

        /**
         * Called when the control element is ready.
         * @param {HTMLElement} packedElement The DOM element of the packed element.
         * @param {HTMLElement} unpackedElement The DOM element of the unpacked element.
         */
        public onReady(packedElement: HTMLElement, unpackedElement: HTMLElement): void {
            this.context.logger.logInformational("Executing onReady!");
            ko.applyBindingsToNode(unpackedElement, {
                template: {
                    name: "Microsoft_Pos_Extensibility_Samples_UnpackedCartAmountDueItem",
                    data: this
                }
            });

            ko.applyBindingsToNode(packedElement, {
                template: {
                    name: "Microsoft_Pos_Extensibility_Samples_PackedCartAmountDueItem",
                    data: this
                }
            });
        }

        /**
         * Initializes the control.
         * @param {ICustomPackingItemState} state The custom control state.
         */
        public init(state: ICustomPackingItemState): void {
            return;
        }

        /**
         * Disposes the control releasing its resources.
         */
        public dispose(): void {
            this._amountDueSubscription.dispose();
            super.dispose();
        }

        /**
         * Method used to handle the onClick of the custom packing item.
         */
        public onItemClickedHandler(): void {
            const correlationId: string = this.context.logger.getNewCorrelationId();
            let cartViewOptions: ClientEntities.CartViewNavigationParameters = new ClientEntities.CartViewNavigationParameters(correlationId);

            this.context.logger.logInformational("Cart amount due packing item clicked.", correlationId);

            this.context.navigator.navigateToPOSView("CartView", cartViewOptions);
        }

        /**
         * Handler for the cart changed event.
         * @param {CartChangedData} data The data sent with the event.
         */
        private _cartChangedHandler(data: CartChangedData): void {
            this.context.logger.logInformational("CartChanged received.");
            this._currentAmountDue(data.cart.AmountDue);
        }
    }
    ```

8. <span data-ttu-id="f4db3-148">**HeaderExtensionSample** フォルダーで、**manifest.json** という JavaScript Object Notation (JSON) ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-148">In the **HeaderExtensionSample** folder, create a JavaScript Object Notation (JSON) file that is named **manifest.json**.</span></span>
9. <span data-ttu-id="f4db3-149">次のコードをコピーして、ファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-149">Copy the following code, and paste it into the file.</span></span>

    ```typescript
    {
        "$schema": "../schemas/manifestSchema.json",
        "name": "HeaderExtensionSample ",
        "publisher": "Microsoft",
        "version": "10.0.14",
        "minimumPosVersion": "9.24.0.0",
        "components": {
            "extend": {
                "header": {
                    "customPackingItems": [
                        {
                            "name": " CartAmountDuePackingItem",
                            "description": "An item showing amount due.",
                            "modulePath": " CartAmountDuePackingItem",
                            "htmlPath": " CartAmountDuePackingItem.html"
                        }
                    ]
                }
            }
        }
    }
    ```

10. <span data-ttu-id="f4db3-150">**POS.Extensions** プロジェクトで、**extensions.json** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-150">In the **POS.Extensions** project, open the **extensions.json** file.</span></span>
11. <span data-ttu-id="f4db3-151">**HeaderExtensionSample** パッケージの詳細を更新して、初回の読み込み時に POS がこの拡張機能パッケージを含めることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="f4db3-151">Update the details of the **HeaderExtensionSample** package, so that the POS can include this extension package during the initial load.</span></span>

    ```typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "HeaderExtensionSample"
            }
        ]
    }
    ```

12. <span data-ttu-id="f4db3-152">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-152">Build the project.</span></span>

### <a name="validate-the-customization"></a><span data-ttu-id="f4db3-153">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="f4db3-153">Validate the customization</span></span>

<span data-ttu-id="f4db3-154">カスタマイズを検証するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f4db3-154">Follow these steps to validate the customization.</span></span>

1. <span data-ttu-id="f4db3-155">オペレーター ID およびパスワードを入力して POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="f4db3-155">Sign in to the POS by entering the operator ID and password.</span></span>
2. <span data-ttu-id="f4db3-156">ヘッダー バーを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4db3-156">Look at the header bar.</span></span> <span data-ttu-id="f4db3-157">追加したカスタム ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-157">The custom button that you added should be visible.</span></span>

<span data-ttu-id="f4db3-158">[POS 設定ページ](view-pos-extension-package-details.md) で、拡張機能パッケージの状態を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f4db3-158">You can view the status of the extension package on the [POS settings page](view-pos-extension-package-details.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]