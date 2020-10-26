---
title: カスタム ボタンを POS ヘッダー バーに追加
description: このトピックでは、POS ヘッダー バーに新しいカスタム ボタンを追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 09-16-2020
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: cd35bffd3b5c1da34df68fff98e827fd030dd870
ms.sourcegitcommit: 0c10539e28de0241859b9ab056547eb34efde98e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2020
ms.locfileid: "3884667"
---
# <a name="add-custom-buttons-to-the-pos-header-bar"></a>カスタム ボタンを POS ヘッダー バーに追加

[!include [banner](../includes/banner.md)]

このトピックでは、販売時点管理 (POS) ヘッダー バーに新しいカスタム ボタンを追加する方法について説明します。 POS ヘッダー バー拡張機能は、Microsoft Dynamics 365 Commerce バージョン 10.0.14 以降でサポートされています。

カスタム ヘッダー ボタンには、コントロール ユーザー インターフェイス (UI)、スタイル、およびテーマを説明するカスケード スタイル シート (CSS) コードを含む HTML ファイルが含まれている必要があります。 また、ロジックを指定する TypeScript ビュー モデル ファイルも含まれている必要があります。 ファイル ビュー モデル ファイル内のクラスは、ヘッダー ボタンのプロパティおよびイベントを継承するために、**CustomPackingItem** クラスを拡張する必要があります。 **cartChangedHandler** イベントは、カート内で何らかの変更があった場合に通知を行うために、ヘッダー ボタンで公開されています。 拡張コードは、カート イベントに基づくカスタム ロジックを実行することも、カスタム ビジネス ロジックを実行することもできます。

## <a name="custompackingitem-class"></a>CustomPackingItem クラス

### <a name="properties"></a>プロパティ

| プロパティ | 説明 |
|----------|-------------|
| CustomPackingItemPosition | POS ヘッダー品目に対する品目の位置。 |
| ICustomPackingItemContext | カスタム ヘッダー梱包品目のコンテキスト。 |

### <a name="events-and-methods"></a>イベントおよびメソッド

| イベントまたはメソッド | 説明 |
|-----------------|-------------|
| cartChangedHandler | **CartUpdated** イベントのハンドラー。 |
| コンストラクター (ID: 文字列、コンテキスト: ICustomPackingItemContext) | このメソッドは、**CustomHeaderPackingItem** クラスの新しいインスタンスを作成します。 |
| ID() | このメソッドは、カスタム ヘッダー梱包品目の ID を取得します。 |
| 表示の取得 (): ブール値 | このメソッドは、表示される値を取得します。 |
| 表示設定 (isVisible: ブール値) | このメソッドは、表示される値を設定します。 |
| 抽象 onReady (packedElement: HTMLElement、unpackedElement: HTMLElement): 無効 | このメソッドは、コントロール要素の準備ができたら、呼び出されます。 |
| 処分 (): 無効 | このメソッドは、コントロールを破棄してリソースを解放します。 |
| 保護された抽象 init (状態: ICustomPackingItemState): 無効 | このメソッドは、コントロールを初期化します。 |

次の例に示すように、**manifest.json** ファイルにヘッダー ボタン拡張機能のノードを追加する必要があります。

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

## <a name="add-a-custom-button-to-the-pos-header-bar"></a>カスタム ボタンを POS ヘッダー バーに追加

次の手順に従って、ヘッダー バーにカスタム ボタンを追加し、請求額をカートから読み取って表示します。

1. Visual Studio 2017 を開きます。
2. **\\RetailSDK\\POS** から **ModernPOS/CloudPOS** ソリューションを開きます。
3. **POS.Extensions** プロジェクトで、**HeaderExtensionSample** というフォルダーを作成します。
4. **HeaderExtensionSample** フォルダーで、**CartAmountDuePackingItem.html** という HTML ファイルを作成します。
5. 次のコードをコピーして、ファイルに貼り付けます。

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

6. **HeaderExtensionSample** フォルダーで、**CartAmountDuePackingItem.ts** という TypeScript ファイルを作成します。
7. 次のコードをコピーして、ファイルに貼り付けます。

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

8. **HeaderExtensionSample** フォルダーで、**manifest.json** という JavaScript Object Notation (JSON) ファイルを作成します。
9. 次のコードをコピーして、ファイルに貼り付けます。

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

10. **POS.Extensions** プロジェクトで、**extensions.json** ファイルを開きます。
11. **HeaderExtensionSample** パッケージの詳細を更新して、初回の読み込み時に POS がこの拡張機能パッケージを含めることができるようにします。

    ```typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "HeaderExtensionSample"
            }
        ]
    }
    ```

12. プロジェクトを構築します。

### <a name="validate-the-customization"></a>カスタマイズの検証

カスタマイズを検証するには、これらの手順に従います。

1. オペレーター ID およびパスワードを入力して POS にサインインします。
2. ヘッダー バーを確認します。 追加したカスタム ボタンが表示されます。

[POS 設定ページ](view-pos-extension-package-details.md) で、拡張機能パッケージの状態を表示できます。
