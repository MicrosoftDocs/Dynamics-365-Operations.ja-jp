---
title: POS カートのビュー イベントとハンドラー
description: この記事では、拡張機能がカスタム シナリオの販売時点管理 (POS) ビュー イベントとハンドラーを使用する方法について説明します。
author: josaw1
ms.date: 02/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 2071e46236d03f912518d99ca8a109121a4b4d93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284335"
---
# <a name="pos-cart-view-events-and-handlers"></a>POS カートのビュー イベントとハンドラー

[!include [banner](../../includes/banner.md)]

この記事では、拡張機能がカスタム シナリオの販売時点管理 (POS) ビュー イベントとハンドラーを使用する方法について説明します。 たとえば、POS のカート ビューは、イベントに基づいて拡張機能がカスタムの業務フローを実行できるよう、複数のイベントとハンドラーを公開します。 拡張機能では、イベントにサブスクライブし、そのイベントが発生するときに通知を受け取ることができます。

## <a name="cart-view-event-handlers"></a>カート ビュー イベント ハンドラー

カート ビュー ハンドラーの消費に使用される基底クラスは **CartExtensionViewControllerBase** です。

```typescript
export default class CartViewController extends CartView.CartExtensionViewControllerBase {
}
```

| 基底クラス                      | イベント/ハンドラー | 説明 |
|---------------------------------|---------------|-------------|
| CartExtensionViewControllerBase | cartLineSelectedHandler: (データ: CartLineSelectedData) =\> 無効; | カート行が選択されたときに表示されるメッセージのハンドラー。 |
|                                 | cartLineSelectionClearedHandler: () =\> 無効; | カート行の選択がクリアされたときに表示されるメッセージのハンドラー。 |
|                                 | tenderLineSelectedHandler: (データ: TenderLineSelectedData) =\> 無効; | 支払/入金の明細行が選択されたときに表示されるメッセージのハンドラー。 |
|                                 | 保護された tenderLineSelectionClearedHandler: () =\> 無効; | 支払/入金の明細行の選択がクリアされたときに表示されるメッセージのハンドラー。 |
|                                 | 保護された cartChangedHandler: (data: CartChangedData) =\> 無効; | カートが変更されたときに表示されるメッセージのハンドラー。 |
|                                 | 保護された processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> 無効; | 品目または顧客の処理状態に関するメッセージを追加するハンドラー。 |
|                                 | 保護された setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): 無効; | ページに表示されるカート行を選択するハンドラー。 |

次の例では、カート ビュー イベントの使用方法を示します。

```typescript
import { ProxyEntities } from "PosApi/Entities";
import { IExtensionCartViewControllerContext } from "PosApi/Extend/Views/CartView";
import * as CartView from "PosApi/Extend/Views/CartView";
import { ArrayExtensions, StringExtensions } from "PosApi/TypeExtensions";

export default class CartViewController extends CartView.CartExtensionViewControllerBase {

    public static selectedCartLineId: string = StringExtensions.EMPTY;

    private _selectedCartLines: ProxyEntities.CartLine[];
    private _selectedTenderLines: ProxyEntities.TenderLine[];
    private _isProcessingAddItemOrCustomer: boolean;

    /**
     * Creates a new instance of the CartViewController class.
     * @param {IExtensionCartViewControllerContext} context The events Handler context.
     * @remarks The events handler context contains APIs through which a handler can communicate with POS.
     */
    constructor(context: IExtensionCartViewControllerContext) {
        super(context);

        this.cartLineSelectedHandler = (data: CartView.CartLineSelectedData): void => {
            this._selectedCartLines = data.cartLines;

            if (ArrayExtensions.hasElements(this._selectedCartLines)) {
                CartViewController.selectedCartLineId = this._selectedCartLines[0].LineId;
            }
        };

        this.cartLineSelectionClearedHandler = (): void => {
            this._selectedCartLines = undefined;
            CartViewController.selectedCartLineId = null;
        };

        this.tenderLineSelectedHandler = (data: CartView.TenderLineSelectedData): void => {
            this._selectedTenderLines = data.tenderLines;
        };

        this.tenderLineSelectionClearedHandler = (): void => {
            this._selectedCartLines = undefined;
        };

        this.processingAddItemOrCustomerChangedHandler = (processing: boolean): void => {
            this._isProcessingAddItemOrCustomer = processing;
        };
    }
}
```

## <a name="base-classes-for-consuming-cart-view-events-in-cart-view-ui-extensions"></a>カート ビューの UI 拡張機能のカート ビュー イベントを使用する基底クラス

ユーザー インターフェイス (UI) でイベントを使用する基底クラスがいくつかあります。

+ カスタム コントロール
+ **合計** ウィンドウのカスタム フィールド
+ **行** グリッドのカスタム列
+ **支払** グリッドのカスタム列
+ **出荷** グリッドのカスタム列

### <a name="custom-controls"></a>カスタム コントロール

| 基底クラス                | イベント | 説明 |
|---------------------------|-------|-------------|
| CartViewCustomControlBase | cartLineSelectedHandler: (データ: CartLineSelectedData) =\> 無効; | カート行が選択されたときに表示されるメッセージのハンドラー。 |
|                           | cartLineSelectionClearedHandler: () =\> 無効; | カート行の選択がクリアされたときに表示されるメッセージのハンドラー。 |
|                           | tenderLineSelectedHandler: (データ: TenderLineSelectedData) =\> 無効; | 支払/入金の明細行が選択されたときに表示されるメッセージのハンドラー。 |
|                           | 保護された tenderLineSelectionClearedHandler: () =\> 無効; | 支払/入金の明細行の選択がクリアされたときに表示されるメッセージのハンドラー。 |
|                           | 保護された cartChangedHandler: (data: CartChangedData) =\> 無効; | カートが変更されたときに表示されるメッセージのハンドラー。 |
|                           | 保護された processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> 無効; | 品目または顧客の処理状態に関するメッセージを追加するハンドラー。 |
|                           | 保護された setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): 無効; | ページに表示されるカート行を選択するハンドラー。 |

### <a name="custom-fields-in-the-totals-pane"></a>合計ウィンドウのカスタム フィールド

| 基底クラス                         | イベント | 説明 |
|------------------------------------|-------|-------------|
| CartViewTotalsPanelCustomFieldBase | 公開 computeValue(cart: ProxyEntities.Cart): 文字列 { } | カスタム フィールドの値を計算します。 |

### <a name="custom-columns-in-the-lines-grid"></a>行グリッドのカスタム列

| 基底クラス                | イベント | 説明 |
|---------------------------|-------|-------------|
| CustomLinesGridColumnBase | 公開タイトル(): 文字列 { } | カスタム列のタイトルを設定します。 |
|                           | 公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 {} | カスタム列の値を計算します。 |
|                           | 公開配置(): CustomGridColumnAlignment { }<p>**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</p> | カスタム列の左側または右側の配置を設定します。 |

### <a name="custom-columns-in-the-payment-grid"></a>支払グリッドのカスタム列

| 基底クラス                   | イベント | 説明 |
|------------------------------|-------|-------------|
| CustomPaymentsGridColumnBase | 公開タイトル(): 文字列 { } | カスタム列のタイトルを設定します。 |
|                              | 公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 { } | カスタム列の値を計算します。 |
|                              | 公開配置(): CustomGridColumnAlignment { }<p>**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</p> | カスタム列の左側または右側の配置を設定します。 |

### <a name="custom-columns-in-the-delivery-grid"></a>出荷グリッドのカスタム列

| 基底クラス                   | イベント | 説明 |
|------------------------------|-------|-------------|
| CustomDeliveryGridColumnBase | 公開タイトル(): 文字列 { } | カスタム列のタイトルを設定します。 |
|                              | 公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 { } | カスタム列の値を計算します。 |
|                              | 公開配置(): CustomGridColumnAlignment { }<p>**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</p> | カスタム列の左側または右側の配置を設定します。 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
