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
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 677b3b36cbfa79bcf5b36a04533eb926429eba17
ms.sourcegitcommit: 45a3564d5ade750e023fa0ab745ba6bca521ca61
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2020
ms.locfileid: "3078936"
---
# <a name="pos-cart-view-events-and-handlers"></a><span data-ttu-id="72596-103">POS カートのビュー イベントとハンドラー</span><span class="sxs-lookup"><span data-stu-id="72596-103">POS Cart view events and handlers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72596-104">このトピックでは、拡張機能がカスタム シナリオの販売時点管理 (POS) ビュー イベントとハンドラーを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="72596-104">This topic explains how extensions can consume the point of sale (POS) view events and handlers for custom scenarios.</span></span> <span data-ttu-id="72596-105">たとえば、POS のカート ビューは、イベントに基づいて拡張機能がカスタムの業務フローを実行できるよう、複数のイベントとハンドラーを公開します。</span><span class="sxs-lookup"><span data-stu-id="72596-105">For example, the Cart view in POS exposes multiple events and handlers so that your extensions can perform custom business flows, based on events.</span></span> <span data-ttu-id="72596-106">拡張機能では、イベントにサブスクライブし、そのイベントが発生するときに通知を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="72596-106">The extensions can subscribe to an event and receive a notification when that event occurs.</span></span>

## <a name="cart-view-event-handlers"></a><span data-ttu-id="72596-107">カート ビュー イベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="72596-107">Cart view event handlers</span></span>

<span data-ttu-id="72596-108">カート ビュー ハンドラーの消費に使用される基底クラスは **CartExtensionViewControllerBase** です。</span><span class="sxs-lookup"><span data-stu-id="72596-108">The base class that is used to consume the Cart view handlers is **CartExtensionViewControllerBase**.</span></span>

```typescript
export default class CartViewController extends CartView.CartExtensionViewControllerBase {
}
```

| <span data-ttu-id="72596-109">基底クラス</span><span class="sxs-lookup"><span data-stu-id="72596-109">Base class</span></span>                      | <span data-ttu-id="72596-110">イベント/ハンドラー</span><span class="sxs-lookup"><span data-stu-id="72596-110">Event/handler</span></span> | <span data-ttu-id="72596-111">説明</span><span class="sxs-lookup"><span data-stu-id="72596-111">Description</span></span> |
|---------------------------------|---------------|-------------|
| <span data-ttu-id="72596-112">CartExtensionViewControllerBase</span><span class="sxs-lookup"><span data-stu-id="72596-112">CartExtensionViewControllerBase</span></span> | <span data-ttu-id="72596-113">cartLineSelectedHandler: (データ: CartLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-113">cartLineSelectedHandler: (data: CartLineSelectedData) =\> void;</span></span> | <span data-ttu-id="72596-114">カート行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-114">The handler for the message that appears when a cart line is selected.</span></span> |
|                                 | <span data-ttu-id="72596-115">cartLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-115">cartLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="72596-116">カート行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-116">The handler for the message that appears when the selection of a cart line is cleared.</span></span> |
|                                 | <span data-ttu-id="72596-117">tenderLineSelectedHandler: (データ: TenderLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-117">tenderLineSelectedHandler: (data: TenderLineSelectedData) =\> void;</span></span> | <span data-ttu-id="72596-118">支払/入金の明細行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-118">The handler for the message that appears when a tender line is selected.</span></span> |
|                                 | <span data-ttu-id="72596-119">保護された tenderLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-119">protected tenderLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="72596-120">支払/入金の明細行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-120">The handler for the message that appears when the selection of a tender line is cleared.</span></span> |
|                                 | <span data-ttu-id="72596-121">保護された cartChangedHandler: (data: CartChangedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-121">protected cartChangedHandler: (data: CartChangedData) =\> void;</span></span> | <span data-ttu-id="72596-122">カートが変更されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-122">The handler for the message that appears when the cart is changed.</span></span> |
|                                 | <span data-ttu-id="72596-123">保護された processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-123">protected processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> void;</span></span> | <span data-ttu-id="72596-124">品目または顧客の処理状態に関するメッセージを追加するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-124">The handler that adds the message about the item or customer processing state.</span></span> |
|                                 | <span data-ttu-id="72596-125">保護された setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-125">protected setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): void;</span></span> | <span data-ttu-id="72596-126">ページに表示されるカート行を選択するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-126">The handler that selects the cart lines that are shown on the page.</span></span> |

<span data-ttu-id="72596-127">次の例では、カート ビュー イベントの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="72596-127">The following example shows how to consume Cart view events.</span></span>

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

## <a name="base-classes-for-consuming-cart-view-events-in-cart-view-ui-extensions"></a><span data-ttu-id="72596-128">カート ビューの UI 拡張機能のカート ビュー イベントを使用する基底クラス</span><span class="sxs-lookup"><span data-stu-id="72596-128">Base classes for consuming Cart view events in Cart view UI extensions</span></span>

<span data-ttu-id="72596-129">ユーザー インターフェイス (UI) でイベントを使用する基底クラスがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="72596-129">There are several base classes for consuming events in the user interface (UI):</span></span>

+ <span data-ttu-id="72596-130">カスタム コントロール</span><span class="sxs-lookup"><span data-stu-id="72596-130">Custom controls</span></span>
+ <span data-ttu-id="72596-131">**合計**ウィンドウのカスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="72596-131">Custom fields in the **Totals** pane</span></span>
+ <span data-ttu-id="72596-132">**行**グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="72596-132">Custom columns in the **Lines** grid</span></span>
+ <span data-ttu-id="72596-133">**支払**グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="72596-133">Custom columns in the **Payment** grid</span></span>
+ <span data-ttu-id="72596-134">**出荷**グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="72596-134">Custom columns in the **Delivery** grid</span></span>

### <a name="custom-controls"></a><span data-ttu-id="72596-135">カスタム コントロール</span><span class="sxs-lookup"><span data-stu-id="72596-135">Custom controls</span></span>

| <span data-ttu-id="72596-136">基底クラス</span><span class="sxs-lookup"><span data-stu-id="72596-136">Base class</span></span>                | <span data-ttu-id="72596-137">イベント</span><span class="sxs-lookup"><span data-stu-id="72596-137">Event</span></span> | <span data-ttu-id="72596-138">説明</span><span class="sxs-lookup"><span data-stu-id="72596-138">Description</span></span> |
|---------------------------|-------|-------------|
| <span data-ttu-id="72596-139">CartViewCustomControlBase</span><span class="sxs-lookup"><span data-stu-id="72596-139">CartViewCustomControlBase</span></span> | <span data-ttu-id="72596-140">cartLineSelectedHandler: (データ: CartLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-140">cartLineSelectedHandler: (data: CartLineSelectedData) =\> void;</span></span> | <span data-ttu-id="72596-141">カート行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-141">The handler for the message that appears when a cart line is selected.</span></span> |
|                           | <span data-ttu-id="72596-142">cartLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-142">cartLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="72596-143">カート行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-143">The handler for the message that appears when the selection of a cart line is cleared.</span></span> |
|                           | <span data-ttu-id="72596-144">tenderLineSelectedHandler: (データ: TenderLineSelectedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-144">tenderLineSelectedHandler: (data: TenderLineSelectedData) =\> void;</span></span> | <span data-ttu-id="72596-145">支払/入金の明細行が選択されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-145">The handler for the message that appears when a tender line is selected.</span></span> |
|                           | <span data-ttu-id="72596-146">保護された tenderLineSelectionClearedHandler: () =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-146">protected tenderLineSelectionClearedHandler: () =\> void;</span></span> | <span data-ttu-id="72596-147">支払/入金の明細行の選択がクリアされたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-147">The handler for the message that appears when the selection of a tender line is cleared.</span></span> |
|                           | <span data-ttu-id="72596-148">保護された cartChangedHandler: (data: CartChangedData) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-148">protected cartChangedHandler: (data: CartChangedData) =\> void;</span></span> | <span data-ttu-id="72596-149">カートが変更されたときに表示されるメッセージのハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-149">The handler for the message that appears when the cart is changed.</span></span> |
|                           | <span data-ttu-id="72596-150">保護された processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-150">protected processingAddItemOrCustomerChangedHandler: (processing: boolean) =\> void;</span></span> | <span data-ttu-id="72596-151">品目または顧客の処理状態に関するメッセージを追加するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-151">The handler that adds the message about the item or customer processing state.</span></span> |
|                           | <span data-ttu-id="72596-152">保護された setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): 無効;</span><span class="sxs-lookup"><span data-stu-id="72596-152">protected setSelectedCartLines(setSelectedCartLinesData: SetSelectedCartLinesData): void;</span></span> | <span data-ttu-id="72596-153">ページに表示されるカート行を選択するハンドラー。</span><span class="sxs-lookup"><span data-stu-id="72596-153">The handler that selects the cart lines that are shown on the page.</span></span> |

### <a name="custom-fields-in-the-totals-pane"></a><span data-ttu-id="72596-154">合計ウィンドウのカスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="72596-154">Custom fields in the Totals pane</span></span>

| <span data-ttu-id="72596-155">基底クラス</span><span class="sxs-lookup"><span data-stu-id="72596-155">Base class</span></span>                         | <span data-ttu-id="72596-156">イベント</span><span class="sxs-lookup"><span data-stu-id="72596-156">Event</span></span> | <span data-ttu-id="72596-157">説明</span><span class="sxs-lookup"><span data-stu-id="72596-157">Description</span></span> |
|------------------------------------|-------|-------------|
| <span data-ttu-id="72596-158">CartViewTotalsPanelCustomFieldBase</span><span class="sxs-lookup"><span data-stu-id="72596-158">CartViewTotalsPanelCustomFieldBase</span></span> | <span data-ttu-id="72596-159">公開 computeValue(cart: ProxyEntities.Cart): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="72596-159">public computeValue(cart: ProxyEntities.Cart): string { }</span></span> | <span data-ttu-id="72596-160">カスタム フィールドの値を計算します。</span><span class="sxs-lookup"><span data-stu-id="72596-160">Compute the value for the custom field.</span></span> |

### <a name="custom-columns-in-the-lines-grid"></a><span data-ttu-id="72596-161">行グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="72596-161">Custom columns in the Lines grid</span></span>

| <span data-ttu-id="72596-162">基底クラス</span><span class="sxs-lookup"><span data-stu-id="72596-162">Base class</span></span>                | <span data-ttu-id="72596-163">イベント</span><span class="sxs-lookup"><span data-stu-id="72596-163">Event</span></span> | <span data-ttu-id="72596-164">説明</span><span class="sxs-lookup"><span data-stu-id="72596-164">Description</span></span> |
|---------------------------|-------|-------------|
| <span data-ttu-id="72596-165">CustomLinesGridColumnBase</span><span class="sxs-lookup"><span data-stu-id="72596-165">CustomLinesGridColumnBase</span></span> | <span data-ttu-id="72596-166">公開タイトル(): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="72596-166">public title(): string { }</span></span> | <span data-ttu-id="72596-167">カスタム列のタイトルを設定します。</span><span class="sxs-lookup"><span data-stu-id="72596-167">Set the title for the custom column.</span></span> |
|                           | <span data-ttu-id="72596-168">公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 {}</span><span class="sxs-lookup"><span data-stu-id="72596-168">public computeValue(cartLine: ProxyEntities.CartLine): string {}</span></span> | <span data-ttu-id="72596-169">カスタム列の値を計算します。</span><span class="sxs-lookup"><span data-stu-id="72596-169">Compute the value for the custom column.</span></span> |
|                           | <span data-ttu-id="72596-170">公開配置(): CustomGridColumnAlignment { }</span><span class="sxs-lookup"><span data-stu-id="72596-170">public alignment(): CustomGridColumnAlignment { }</span></span><p><span data-ttu-id="72596-171">**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</span><span class="sxs-lookup"><span data-stu-id="72596-171">**Supported values:** enum CustomGridColumnAlignment { Left = 0, Right = 1 }</span></span></p> | <span data-ttu-id="72596-172">カスタム列の左側または右側の配置を設定します。</span><span class="sxs-lookup"><span data-stu-id="72596-172">Set left or right alignment for the custom column.</span></span> |

### <a name="custom-columns-in-the-payment-grid"></a><span data-ttu-id="72596-173">支払グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="72596-173">Custom columns in the Payment grid</span></span>

| <span data-ttu-id="72596-174">基底クラス</span><span class="sxs-lookup"><span data-stu-id="72596-174">Base class</span></span>                   | <span data-ttu-id="72596-175">イベント</span><span class="sxs-lookup"><span data-stu-id="72596-175">Event</span></span> | <span data-ttu-id="72596-176">説明</span><span class="sxs-lookup"><span data-stu-id="72596-176">Description</span></span> |
|------------------------------|-------|-------------|
| <span data-ttu-id="72596-177">CustomPaymentsGridColumnBase</span><span class="sxs-lookup"><span data-stu-id="72596-177">CustomPaymentsGridColumnBase</span></span> | <span data-ttu-id="72596-178">公開タイトル(): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="72596-178">public title(): string { }</span></span> | <span data-ttu-id="72596-179">カスタム列のタイトルを設定します。</span><span class="sxs-lookup"><span data-stu-id="72596-179">Set the title for the custom column.</span></span> |
|                              | <span data-ttu-id="72596-180">公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="72596-180">public computeValue(cartLine: ProxyEntities.CartLine): string { }</span></span> | <span data-ttu-id="72596-181">カスタム列の値を計算します。</span><span class="sxs-lookup"><span data-stu-id="72596-181">Compute the value for the custom column.</span></span> |
|                              | <span data-ttu-id="72596-182">公開配置(): CustomGridColumnAlignment { }</span><span class="sxs-lookup"><span data-stu-id="72596-182">public alignment(): CustomGridColumnAlignment { }</span></span><p><span data-ttu-id="72596-183">**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</span><span class="sxs-lookup"><span data-stu-id="72596-183">**Supported values:** enum CustomGridColumnAlignment { Left = 0, Right = 1 }</span></span></p> | <span data-ttu-id="72596-184">カスタム列の左側または右側の配置を設定します。</span><span class="sxs-lookup"><span data-stu-id="72596-184">Set left or right alignment for the custom column.</span></span> |

### <a name="custom-columns-in-the-delivery-grid"></a><span data-ttu-id="72596-185">出荷グリッドのカスタム列</span><span class="sxs-lookup"><span data-stu-id="72596-185">Custom columns in the Delivery grid</span></span>

| <span data-ttu-id="72596-186">基底クラス</span><span class="sxs-lookup"><span data-stu-id="72596-186">Base class</span></span>                   | <span data-ttu-id="72596-187">イベント</span><span class="sxs-lookup"><span data-stu-id="72596-187">Event</span></span> | <span data-ttu-id="72596-188">説明</span><span class="sxs-lookup"><span data-stu-id="72596-188">Description</span></span> |
|------------------------------|-------|-------------|
| <span data-ttu-id="72596-189">CustomDeliveryGridColumnBase</span><span class="sxs-lookup"><span data-stu-id="72596-189">CustomDeliveryGridColumnBase</span></span> | <span data-ttu-id="72596-190">公開タイトル(): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="72596-190">public title(): string { }</span></span> | <span data-ttu-id="72596-191">カスタム列のタイトルを設定します。</span><span class="sxs-lookup"><span data-stu-id="72596-191">Set the title for the custom column.</span></span> |
|                              | <span data-ttu-id="72596-192">公開 computeValue(cartLine: ProxyEntities.CartLine): 文字列 { }</span><span class="sxs-lookup"><span data-stu-id="72596-192">public computeValue(cartLine: ProxyEntities.CartLine): string { }</span></span> | <span data-ttu-id="72596-193">カスタム列の値を計算します。</span><span class="sxs-lookup"><span data-stu-id="72596-193">Compute the value for the custom column.</span></span> |
|                              | <span data-ttu-id="72596-194">公開配置(): CustomGridColumnAlignment { }</span><span class="sxs-lookup"><span data-stu-id="72596-194">public alignment(): CustomGridColumnAlignment { }</span></span><p><span data-ttu-id="72596-195">**サポートされている値:** 列挙 CustomGridColumnAlignment { 左 = 0, 右 = 1 }</span><span class="sxs-lookup"><span data-stu-id="72596-195">**Supported values:** enum CustomGridColumnAlignment { Left = 0, Right = 1 }</span></span></p> | <span data-ttu-id="72596-196">カスタム列の左側または右側の配置を設定します。</span><span class="sxs-lookup"><span data-stu-id="72596-196">Set left or right alignment for the custom column.</span></span> |
