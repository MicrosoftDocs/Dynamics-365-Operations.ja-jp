---
title: Modern POS (MPOS) トランザクション ページへのカスタム コントロールの追加
description: このトピックでは、画面レイアウト デザイナーを使用して トランザクション ページに新しいカスタム コントロールを追加する方法について説明します。
author: mugunthanm
ms.date: 11/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 24411
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-11-22
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d2ff1937101eaeb585b3e2606b847724ffed7a78
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795663"
---
# <a name="add-custom-controls-to-modern-pos-mpos-transaction-pages"></a>Modern POS (MPOS) トランザクション ページへのカスタム コントロールの追加

[!include [banner](../../includes/banner.md)]

カスタム コントロールを使用して、トランザクション ページにさらに情報を追加することができます。 画面レイアウト デザイナーを使用して、トランザクション ページにカスタム コントロールを追加することができます。 デザイナーで、ドラッグ アンド ドロップ操作を使用してカスタム コントロールを追加してから、コントロールの位置、高さ、および幅を設定できます。 POS 拡張フレームワークを使用して、独自の拡張機能にカスタム コントロール用ビジネス ロジックを実装することができます。 このトピックでは、選択した行の項目、項目 ID、および説明の詳細を示す新しいカスタム コントロールを追加する方法について説明します。

> [!NOTE]
> このトピックでは Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 Retail プラットフォーム更新 8 と Retail アプリ更新プログラム 4 修正プログラムが適用されます。

## <a name="add-a-new-custom-control"></a>新しいカスタム コントロールの追加

1. Dynamics 365 Commerce へサインインします。
2. **Retail** > **チャネル設定** > **POS 設定** > **POS** > **画面レイアウト** と選択します。
3. **F3MGR** 画面レイアウト ID を選択した後、アクション ウィンドウで **デザイナー** を選択します。
4. レイアウト サイズとして **1440 x 960: フル レイアウト** を選択し、**レイアウト デザイナー** を選択します。
5. デザイナー ツールをインストールするように求められたら、**開く** を選択し、インストール手順に従います。
6. Azure Active Directory (Azure AD) の資格情報の入力を要求するメッセージが表示されたら、その情報を入力してデザイナーを起動します。
7. デザイナーで、カスタム コントロールを左ウィンドウからページにドラッグして、必要に応じてカスタム コントロールを調整、サイズ変更、または位置変更します。
8. ページで、カスタム コントロールを右クリックし、**カスタマイズ** を選択します。
9. ダイアログ ボックスで、これらのプロパティを設定します。

   - **コントロール名:** lineDetails
   - **パッケージ名:** Pos_Extensibility_Samples
   - **パブリッシャー名:** Contoso

     > [!NOTE]
     > これらの名前は、拡張子マニフェスト内の名前と一致する必要があります。

10. **閉じる** ボタン (**X**) を選択し、デザイナーを閉じます。
11. 変更の保存を求められたら、**はい** を選択します。 **いいえ** を選択した場合、変更は保存されません。
12. **小売** > **小売 IT** > **配送スケジュール** の順に選択します。
13. **1090 レジスター** ジョブを選択し、**今すぐ実行** を選択します。

## <a name="add-business-logic-to-the-custom-control"></a>カスタム コントロールへのビジネス ロジックの追加

1. Microsoft Visual Studio 2015 を管理者として起動します。
2. **ModernPOS** ソリューションを **…\RetailSDK\POS** から開きます。
3. **POS.Extensions** プロジェクトで、**CustomControlExtensions** というフォルダーを作成します。
4. **CustomControlExtensions** フォルダーで、**Cart** というフォルダーを作成します。
5. **カート** フォルダーで、**CartViewController.ts** という Typescript ファイルを作成します。
6. **CartViewController.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { IExtensionCartViewControllerContext } from "PosApi/Extend/Views/CartView";
    import * as CartView from "PosApi/Extend/Views/CartView";
    ```

7. **CartViewController** という名前のクラスを作成し、**CartExtensionViewControllerBase** からクラスを拡張します。 **CartExtensionViewControllerBase** クラスには、買い物カゴおよび支払/入金の明細行、カートの明細行の選択ハンドラー、買い物カゴの明細行がクリアされたハンドラーが含まれています。 これらの要素は、カスタム コントロールで選択した行を表示するために使用されます。

    ```typescript
    export default class CartViewController extends CartView.CartExtensionViewControllerBase {

    }
    ```

8. **CartViewController** クラスで、選択したカート明細行および支払/入金明細行を取得する 2 つのプライベート変数を追加します。

    ```typescript
    private _selectedCartLines: ProxyEntities.CartLine[];

    private _selectedTenderLines: ProxyEntities.TenderLine[];
    ```

9. カートと入金の選択情報を設定するクラス **コンストラクター** メソッドを作成します。

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

    全体的なクラスは、次のようになります。

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

10. **カート** フォルダーで、**LineDetailsCustomControl.html** という HTML ファイルを作成します。
11. **LineDetailsCustomControl.html** ファイルで、選択した明細行項目の ID と説明を表示する 2 つのテキスト フィールドを追加します。 既定のコードを削除し、次のコードを追加します。

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

15. クラスを作成し、**CartViewCustomControlBase** からクラスを拡張します。

    ```typescript
    export default class LineDetailsCustomControl extends CartViewCustomControlBase {}
    ```

16. 次のプライベート変数を宣言し、買い物カゴの品目 ID と説明を設定します。

    ```typescript
    private static readonly TEMPLATE_ID: string = "Microsoft_Pos_Extensibility_Samples_LineDetails";
    public readonly cartLineItemId: Computed<string>;
    public readonly cartLineDescription: Computed<string>;
    public readonly isCartLineSelected: Computed<boolean>;
    private readonly _cartLine: Observable<ProxyEntities.CartLine>;
    private _state: ICartViewCustomControlState;
    ```

17. **コンストラクター** メソッドを作成して、選択したハンドラーを初期化して取得します。

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

18. **onReady** メソッドを追加して、コントロールを指定した HTML 要素にバインドします。

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

19. **init** メソッドを追加して状態を設定します。

    ```typescript
    public init(state: ICartViewCustomControlState): void {
        this._state = state;
    }
    ```

    全体的なクラスは、次のようになります。

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

20. **CustomControlExtensions** フォルダーで、**manifest.json** という JSON ファイルを作成します。
21. **manifest.json** ファイルに次のコードを追加します。

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

22. **POS.Extensions** プロジェクトで **extensions.json** ファイルを開き、次の **CustomControlExtensions** サンプルで更新して、POS が実行時にこの拡張機能に含まれるようにします。

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

23. **tsconfig.json** ファイルで、除外リストに拡張パッケージ フォルダーをコメントアウトします。 POS は、このファイルを使用して、拡張機能を追加または除外します。 既定では、リストに除外された拡張リスト全体が含まれています。 拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、除外リストの拡張子をコメントアウトします。

    ```typescript
    "exclude": [
        "SampleExtensions"
        //"SampleExtensions2",
        //"CustomControlExtensions"
    ],
    ```

24. プロジェクトをコンパイル、およびリビルドします。

## <a name="validate-the-customization"></a>カスタマイズの検証

1. オペレーター ID に **000160**、パスワードに **123** を使用して Modern POS にサインインします。
2. **ようこそ** 画面で、**現在のトランザクション** ボタンを選択します。
3. トランザクションを任意の品目に追加し、追加した明細行品目を選択します。

    カスタム コントロールには、選択した明細行品目の ID と説明が表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]