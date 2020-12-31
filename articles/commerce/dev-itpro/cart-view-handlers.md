---
title: POS カートのビュー イベントとハンドラー
description: このトピックでは、拡張機能がカスタム シナリオの販売時点管理 (POS) ビュー イベントとハンドラーを使用する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 02/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 026ebbbb586f357d18b4fa6612757d9f171df31b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680384"
---
# <a name="pos-cart-view-events-and-handlers"></a><span data-ttu-id="6f6e3-103">POS カートのビュー イベントとハンドラー</span><span class="sxs-lookup"><span data-stu-id="6f6e3-103">POS Cart view events and handlers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f6e3-104">このトピックでは、拡張機能がカスタム シナリオの販売時点管理 (POS) ビュー イベントとハンドラーを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-104">This topic explains how extensions can consume the point of sale (POS) view events and handlers for custom scenarios.</span></span> <span data-ttu-id="6f6e3-105">たとえば、POS のカート ビューは、イベントに基づいて拡張機能がカスタムの業務フローを実行できるよう、複数のイベントとハンドラーを公開します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-105">For example, the Cart view in POS exposes multiple events and handlers so that your extensions can perform custom business flows, based on events.</span></span> <span data-ttu-id="6f6e3-106">拡張機能では、イベントにサブスクライブし、そのイベントが発生するときに通知を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-106">The extensions can subscribe to an event and receive a notification when that event occurs.</span></span>

## <a name="cart-view-event-handlers"></a><span data-ttu-id="6f6e3-107">カート ビュー イベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="6f6e3-107">Cart view event handlers</span></span>

<span data-ttu-id="6f6e3-108">カート ビュー ハンドラーの消費に使用される基底クラスは **CartExtensionViewControllerBase** です。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-108">The base class that is used to consume the Cart view handlers is **CartExtensionViewControllerBase**.</span></span>

```typescript
export default class CartViewController extends CartView.CartExtensionViewControllerBase {
}
```

| <span data-ttu-id="6f6e3-109">基底クラス</span><span class="sxs-lookup"><span data-stu-id="6f6e3-109">Base class</span></span>                      | <span data-ttu-id="6f6e3-110">イベント/ハンドラー</span><span class="sxs-lookup"><span data-stu-id="6f6e3-110">Event/handler</span></span> | <span data-ttu-id="6f6e3-111">説明</span><span class="sxs-lookup"><span data-stu-id="6f6e3-111">Description</span></span> |
|---------------------------------|---------------|-------------|
| <span data-ttu-id="6f6e3-112">CartExtensionViewControllerBase</span><span class="sxs-lookup"><span data-stu-id="6f6e3-112">CartExtensionViewControllerBase</span></span> | <span data-ttu-id="6f6e3-113">cartLineSelectedHandler: (データ: CartLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-113">cartLineSelectedHandler: (data: CartLineSelectedData) =\> void;</span></span> | <span data-ttu-id="6f6e3-114">カート行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-114">The handler for the message that appears when a cart line is selected.</span></span> |
|                                 | <span data-ttu-id="6f6e3-115">cartLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-115">cartLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="6f6e3-116">カート行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-116">The handler for the message that appears when the selection of a cart line is cleared.</span></span> |
|                                 | <span data-ttu-id="6f6e3-117">tenderLineSelectedHandler: (データ: TenderLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-117">tenderLineSelectedHandler: (data: TenderLineSelectedData) =\> void;</span></span> | <span data-ttu-id="6f6e3-118">支払/入金の明細行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-118">The handler for the message that appears when a tender line is selected.</span></span> |
|                                 | <span data-ttu-id="6f6e3-119">保護された tenderLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-119">protected tenderLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="6f6e3-120">支払/入金の明細行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-120">The handler for the message that appears when the selection of a tender line is cleared.</span></span> |
|                                 | <span data-ttu-id="6f6e3-121">保護された cartChangedHandler: (data: CartChangedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-121">protected cartChangedHandler: (data: CartChangedData) =\> void;</span></span> | <span data-ttu-id="6f6e3-122">カートが変更されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-122">The handler for the message that appears when the cart is changed.</span></span> |
|                                 | <span data-ttu-id="6f6e3-123">保護された processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-123">protected processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> void;</span></span> | <span data-ttu-id="6f6e3-124">品目または顧客の処理状態に関するメッセージを追加するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-124">The handler that adds the message about the item or customer processing state.</span></span> |
|                                 | <span data-ttu-id="6f6e3-125">保護された setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-125">protected setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): void;</span></span> | <span data-ttu-id="6f6e3-126">ページに表示されるカート行を選択するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-126">The handler that selects the cart lines that are shown on the page.</span></span> |

<span data-ttu-id="6f6e3-127">次の例では、カート ビュー イベントの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-127">The following example shows how to consume Cart view events.</span></span>

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

## <a name="base-classes-for-consuming-cart-view-events-in-cart-view-ui-extensions"></a><span data-ttu-id="6f6e3-128">カート ビューの UI 拡張機能のカート ビュー イベントを使用する基底クラス</span><span class="sxs-lookup"><span data-stu-id="6f6e3-128">Base classes for consuming Cart view events in Cart view UI extensions</span></span>

<span data-ttu-id="6f6e3-129">ユーザー インターフェイス (UI) でイベントを使用する基底クラスがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-129">There are several base classes for consuming events in the user interface (UI):</span></span>

+ <span data-ttu-id="6f6e3-130">カスタム コントロール</span><span class="sxs-lookup"><span data-stu-id="6f6e3-130">Custom controls</span></span>
+ <span data-ttu-id="6f6e3-131">**合計** ウィンドウのカスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="6f6e3-131">Custom fields in the **Totals** pane</span></span>
+ <span data-ttu-id="6f6e3-132">**行** グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="6f6e3-132">Custom columns in the **Lines** grid</span></span>
+ <span data-ttu-id="6f6e3-133">**支払** グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="6f6e3-133">Custom columns in the **Payment** grid</span></span>
+ <span data-ttu-id="6f6e3-134">**出荷** グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="6f6e3-134">Custom columns in the **Delivery** grid</span></span>

### <a name="custom-controls"></a><span data-ttu-id="6f6e3-135">カスタム コントロール</span><span class="sxs-lookup"><span data-stu-id="6f6e3-135">Custom controls</span></span>

| <span data-ttu-id="6f6e3-136">基底クラス</span><span class="sxs-lookup"><span data-stu-id="6f6e3-136">Base class</span></span>                | <span data-ttu-id="6f6e3-137">イベント</span><span class="sxs-lookup"><span data-stu-id="6f6e3-137">Event</span></span> | <span data-ttu-id="6f6e3-138">説明</span><span class="sxs-lookup"><span data-stu-id="6f6e3-138">Description</span></span> |
|---------------------------|-------|-------------|
| <span data-ttu-id="6f6e3-139">CartViewCustomControlBase</span><span class="sxs-lookup"><span data-stu-id="6f6e3-139">CartViewCustomControlBase</span></span> | <span data-ttu-id="6f6e3-140">cartLineSelectedHandler: (データ: CartLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-140">cartLineSelectedHandler: (data: CartLineSelectedData) =\> void;</span></span> | <span data-ttu-id="6f6e3-141">カート行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-141">The handler for the message that appears when a cart line is selected.</span></span> |
|                           | <span data-ttu-id="6f6e3-142">cartLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-142">cartLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="6f6e3-143">カート行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-143">The handler for the message that appears when the selection of a cart line is cleared.</span></span> |
|                           | <span data-ttu-id="6f6e3-144">tenderLineSelectedHandler: (データ: TenderLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-144">tenderLineSelectedHandler: (data: TenderLineSelectedData) =\> void;</span></span> | <span data-ttu-id="6f6e3-145">支払/入金の明細行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-145">The handler for the message that appears when a tender line is selected.</span></span> |
|                           | <span data-ttu-id="6f6e3-146">保護された tenderLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-146">protected tenderLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="6f6e3-147">支払/入金の明細行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-147">The handler for the message that appears when the selection of a tender line is cleared.</span></span> |
|                           | <span data-ttu-id="6f6e3-148">保護された cartChangedHandler: (data: CartChangedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-148">protected cartChangedHandler: (data: CartChangedData) =\> void;</span></span> | <span data-ttu-id="6f6e3-149">カートが変更されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-149">The handler for the message that appears when the cart is changed.</span></span> |
|                           | <span data-ttu-id="6f6e3-150">保護された processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-150">protected processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> void;</span></span> | <span data-ttu-id="6f6e3-151">品目または顧客の処理状態に関するメッセージを追加するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-151">The handler that adds the message about the item or customer processing state.</span></span> |
|                           | <span data-ttu-id="6f6e3-152">保護された setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): 無効;</span><span class="sxs-lookup"><span data-stu-id="6f6e3-152">protected setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): void;</span></span> | <span data-ttu-id="6f6e3-153">ページに表示されるカート行を選択するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-153">The handler that selects the cart lines that are shown on the page.</span></span> |

### <a name="custom-fields-in-the-totals-pane"></a><span data-ttu-id="6f6e3-154">合計ウィンドウのカスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="6f6e3-154">Custom fields in the Totals pane</span></span>

| <span data-ttu-id="6f6e3-155">基底クラス</span><span class="sxs-lookup"><span data-stu-id="6f6e3-155">Base class</span></span>                         | <span data-ttu-id="6f6e3-156">イベント</span><span class="sxs-lookup"><span data-stu-id="6f6e3-156">Event</span></span> | <span data-ttu-id="6f6e3-157">説明</span><span class="sxs-lookup"><span data-stu-id="6f6e3-157">Description</span></span> |
|------------------------------------|-------|-------------|
| <span data-ttu-id="6f6e3-158">CartViewTotalsPanelCustomFieldBase</span><span class="sxs-lookup"><span data-stu-id="6f6e3-158">CartViewTotalsPanelCustomFieldBase</span></span> | <span data-ttu-id="6f6e3-159">公開 computeValue(cart: ProxyEntities.Cart): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-159">public computeValue(cart: ProxyEntities.Cart): string { }</span></span> | <span data-ttu-id="6f6e3-160">カスタム フィールドの値を計算します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-160">Compute the value for the custom field.</span></span> |

### <a name="custom-columns-in-the-lines-grid"></a><span data-ttu-id="6f6e3-161">行グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="6f6e3-161">Custom columns in the Lines grid</span></span>

| <span data-ttu-id="6f6e3-162">基底クラス</span><span class="sxs-lookup"><span data-stu-id="6f6e3-162">Base class</span></span>                | <span data-ttu-id="6f6e3-163">イベント</span><span class="sxs-lookup"><span data-stu-id="6f6e3-163">Event</span></span> | <span data-ttu-id="6f6e3-164">説明</span><span class="sxs-lookup"><span data-stu-id="6f6e3-164">Description</span></span> |
|---------------------------|-------|-------------|
| <span data-ttu-id="6f6e3-165">CustomLinesGridColumnBase</span><span class="sxs-lookup"><span data-stu-id="6f6e3-165">CustomLinesGridColumnBase</span></span> | <span data-ttu-id="6f6e3-166">公開タイトル(): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-166">public title(): string { }</span></span> | <span data-ttu-id="6f6e3-167">カスタム列のタイトルを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-167">Set the title for the custom column.</span></span> |
|                           | <span data-ttu-id="6f6e3-168">公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 {}</span><span class="sxs-lookup"><span data-stu-id="6f6e3-168">public computeValue(cartLine: ProxyEntities.CartLine): string {}</span></span> | <span data-ttu-id="6f6e3-169">カスタム列の値を計算します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-169">Compute the value for the custom column.</span></span> |
|                           | <span data-ttu-id="6f6e3-170">公開配置(): CustomGridColumnAlignment { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-170">public alignment(): CustomGridColumnAlignment { }</span></span><p><span data-ttu-id="6f6e3-171">**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-171">**Supported values:** enum CustomGridColumnAlignment { Left = 0, Right = 1 }</span></span></p> | <span data-ttu-id="6f6e3-172">カスタム列の左側または右側の配置を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-172">Set left or right alignment for the custom column.</span></span> |

### <a name="custom-columns-in-the-payment-grid"></a><span data-ttu-id="6f6e3-173">支払グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="6f6e3-173">Custom columns in the Payment grid</span></span>

| <span data-ttu-id="6f6e3-174">基底クラス</span><span class="sxs-lookup"><span data-stu-id="6f6e3-174">Base class</span></span>                   | <span data-ttu-id="6f6e3-175">イベント</span><span class="sxs-lookup"><span data-stu-id="6f6e3-175">Event</span></span> | <span data-ttu-id="6f6e3-176">説明</span><span class="sxs-lookup"><span data-stu-id="6f6e3-176">Description</span></span> |
|------------------------------|-------|-------------|
| <span data-ttu-id="6f6e3-177">CustomPaymentsGridColumnBase</span><span class="sxs-lookup"><span data-stu-id="6f6e3-177">CustomPaymentsGridColumnBase</span></span> | <span data-ttu-id="6f6e3-178">公開タイトル(): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-178">public title(): string { }</span></span> | <span data-ttu-id="6f6e3-179">カスタム列のタイトルを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-179">Set the title for the custom column.</span></span> |
|                              | <span data-ttu-id="6f6e3-180">公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-180">public computeValue(cartLine: ProxyEntities.CartLine): string { }</span></span> | <span data-ttu-id="6f6e3-181">カスタム列の値を計算します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-181">Compute the value for the custom column.</span></span> |
|                              | <span data-ttu-id="6f6e3-182">公開配置(): CustomGridColumnAlignment { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-182">public alignment(): CustomGridColumnAlignment { }</span></span><p><span data-ttu-id="6f6e3-183">**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-183">**Supported values:** enum CustomGridColumnAlignment { Left = 0, Right = 1 }</span></span></p> | <span data-ttu-id="6f6e3-184">カスタム列の左側または右側の配置を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-184">Set left or right alignment for the custom column.</span></span> |

### <a name="custom-columns-in-the-delivery-grid"></a><span data-ttu-id="6f6e3-185">出荷グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="6f6e3-185">Custom columns in the Delivery grid</span></span>

| <span data-ttu-id="6f6e3-186">基底クラス</span><span class="sxs-lookup"><span data-stu-id="6f6e3-186">Base class</span></span>                   | <span data-ttu-id="6f6e3-187">イベント</span><span class="sxs-lookup"><span data-stu-id="6f6e3-187">Event</span></span> | <span data-ttu-id="6f6e3-188">説明</span><span class="sxs-lookup"><span data-stu-id="6f6e3-188">Description</span></span> |
|------------------------------|-------|-------------|
| <span data-ttu-id="6f6e3-189">CustomDeliveryGridColumnBase</span><span class="sxs-lookup"><span data-stu-id="6f6e3-189">CustomDeliveryGridColumnBase</span></span> | <span data-ttu-id="6f6e3-190">公開タイトル(): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-190">public title(): string { }</span></span> | <span data-ttu-id="6f6e3-191">カスタム列のタイトルを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-191">Set the title for the custom column.</span></span> |
|                              | <span data-ttu-id="6f6e3-192">公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-192">public computeValue(cartLine: ProxyEntities.CartLine): string { }</span></span> | <span data-ttu-id="6f6e3-193">カスタム列の値を計算します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-193">Compute the value for the custom column.</span></span> |
|                              | <span data-ttu-id="6f6e3-194">公開配置(): CustomGridColumnAlignment { }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-194">public alignment(): CustomGridColumnAlignment { }</span></span><p><span data-ttu-id="6f6e3-195">**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</span><span class="sxs-lookup"><span data-stu-id="6f6e3-195">**Supported values:** enum CustomGridColumnAlignment { Left = 0, Right = 1 }</span></span></p> | <span data-ttu-id="6f6e3-196">カスタム列の左側または右側の配置を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f6e3-196">Set left or right alignment for the custom column.</span></span> |
