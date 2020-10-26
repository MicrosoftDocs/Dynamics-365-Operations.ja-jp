---
title: 販売時点管理 (POS) API
description: このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。
author: mugunthanm
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-10-29
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: 6fec60a736bec592707e8816c0f9fef86b83864b
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835840"
---
# <a name="point-of-sale-pos-apis"></a><span data-ttu-id="affd1-103">販売時点管理 (POS) API</span><span class="sxs-lookup"><span data-stu-id="affd1-103">Point of sale (POS) APIs</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="affd1-104">Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="affd1-104">Retail POS APIs help you to easily build extensions or new features to the POS app.</span></span> <span data-ttu-id="affd1-105">たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。</span><span class="sxs-lookup"><span data-stu-id="affd1-105">For example, if you are extending the Retail POS application to add new features in which to want to get product details, change prices, or add items to a cart.</span></span> <span data-ttu-id="affd1-106">これを実現する API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="affd1-106">you can consume APIs that will do the work for you.</span></span> <span data-ttu-id="affd1-107">これを行うには、作業を実行する API を呼び出す必要があるだけです。</span><span class="sxs-lookup"><span data-stu-id="affd1-107">To do this, you need to simply call the APIs to do the work.</span></span> <span data-ttu-id="affd1-108">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="affd1-108">The POS API simplifies the extension pattern and provides continuous support to build the extensions.</span></span>

<span data-ttu-id="affd1-109">拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。</span><span class="sxs-lookup"><span data-stu-id="affd1-109">Extension patterns have been unified across commerce runtime (CRT), POS, and Hardware station (HWS) by following the request/response pattern.</span></span> <span data-ttu-id="affd1-110">すべての POS API は、CRT や HWS のような要求/応答として公開されます。</span><span class="sxs-lookup"><span data-stu-id="affd1-110">All the POS APIs are exposed as request/response like CRT and HWS.</span></span> 

<span data-ttu-id="affd1-111">POS API は、3 つのさまざまなシナリオに分類されます。</span><span class="sxs-lookup"><span data-stu-id="affd1-111">POS APIs are categorized into three different scenarios:</span></span>

- <span data-ttu-id="affd1-112">**消費** - 拡張機能のパブリック API を使用します。</span><span class="sxs-lookup"><span data-stu-id="affd1-112">**Consume** – Consume public APIs in your extension.</span></span>

- <span data-ttu-id="affd1-113">**拡張** - 一部の追加ロジックを実行するパブリック API をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="affd1-113">**Extend** – Override public APIs to do some additional logic.</span></span>

- <span data-ttu-id="affd1-114">**作成** - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="affd1-114">**Create** – Create new APIs using the exposed POS interface, which can be used across extensions.</span></span>

<span data-ttu-id="affd1-115">API の多くは、拡張機能で消費できます。</span><span class="sxs-lookup"><span data-stu-id="affd1-115">Many APIs can be consumed in extensions.</span></span> <span data-ttu-id="affd1-116">たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="affd1-116">For example, if you want to change the price of the item based on an external web service call, you can call PriceOverrideOperationRequest to change the price of the item.</span></span> <span data-ttu-id="affd1-117">消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。</span><span class="sxs-lookup"><span data-stu-id="affd1-117">Within the consume, the APIs are sub categorized by module like cart, peripherals, store operations, etc.</span></span>

> [!NOTE]
> <span data-ttu-id="affd1-118">すべての API の一覧は、**Pos.Api.d.ts** にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。</span><span class="sxs-lookup"><span data-stu-id="affd1-118">A list of the all of the APIs is available in **Pos.Api.d.ts**, which is part of the Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts).</span></span> <span data-ttu-id="affd1-119">拡張機能は、公開されている要求と、POS.Api.d.ts からの応答のみを使用する必要があり、Pos.Api.d.ts を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="affd1-119">Extensions must consume only the exposed request and response from the POS.Api.d.ts and no modification is allowed to Pos.Api.d.ts.</span></span> <span data-ttu-id="affd1-120">拡張機能は、POS API、プロパティ、メソッド、またはハンドラーを、POS Commerce またはセッション オブジェクトから直接使用したり更新したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="affd1-120">Extensions should not consume or update any POS APIs, properties, methods, or handlers directly from POS commerce or sessions objects.</span></span> 

## <a name="how-to-consume-apis-in-your-extension"></a><span data-ttu-id="affd1-121">拡張機能で API を使用する方法</span><span class="sxs-lookup"><span data-stu-id="affd1-121">How to consume APIs in your extension</span></span>

<span data-ttu-id="affd1-122">拡張機能で Retail API を利用するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="affd1-122">Use the following steps to consume Retail APIs in your extensions.</span></span>

1.  <span data-ttu-id="affd1-123">拡張機能ファイルで API をインポートします。</span><span class="sxs-lookup"><span data-stu-id="affd1-123">Import the API in your extension file.</span></span>

    <span data-ttu-id="affd1-124">たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="affd1-124">For example, if you want to consume the save attribute on cart API in your extension, then you need to add the following import statements.</span></span>

    <span data-ttu-id="affd1-125">パターンは、"PosApi/Consume/Module name" からの {api name} のインポートです。</span><span class="sxs-lookup"><span data-stu-id="affd1-125">The pattern is import { api name } from "PosApi/Consume/Module name";</span></span>
 
    ```typescript
    import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
    ```

2.  <span data-ttu-id="affd1-126">必要な場合は、クライアントのエンティティとプロキシ エンティティをインポートします。</span><span class="sxs-lookup"><span data-stu-id="affd1-126">Import the client entities and proxy entities if required.</span></span>

    ```typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
    ```
3.  <span data-ttu-id="affd1-127">API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="affd1-127">Declare the API variable and execute it using the POS runtime, which you can access the runtime by using: this.context.runtime.executeAsync("api name")</span></span>

    ```typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
    ```
    
    <span data-ttu-id="affd1-128">たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="affd1-128">For example, if you want to execute the tender removal, use SaveAttributesOnCartClientRequest api, and refer to the following steps.</span></span>
 
    ```typescript
    let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();

     attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;

     attributeValue.TextValue = "Yes";

     let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];

     let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =

    new SaveAttributesOnCartClientRequest(attributeValues);

    result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
    ```

### <a name="samples-showing-how-to-access-apis"></a><span data-ttu-id="affd1-129">API にアクセスする方法を示すサンプル</span><span class="sxs-lookup"><span data-stu-id="affd1-129">Samples showing how to access APIs</span></span>

<span data-ttu-id="affd1-130">**現在の買い物カゴを取得**</span><span class="sxs-lookup"><span data-stu-id="affd1-130">**Get Current cart**</span></span>
```typescript
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```

<span data-ttu-id="affd1-131">**買い物カゴに追加された現在の顧客を取得**</span><span class="sxs-lookup"><span data-stu-id="affd1-131">**Get Current customer added to cart**</span></span>
```typescript
 // Gets the current customer.

 let result: Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>>;

 if (!ObjectExtensions.isNullOrUndefined(currentCart) && !ObjectExtensions.isNullOrUndefined(currentCart.CustomerId)) {

 let getCurrentCustomerClientRequest: GetCustomerClientRequest<GetCustomerClientResponse> =

 new GetCustomerClientRequest(currentCart.CustomerId);

 result = this.context.runtime.executeAsync<GetCustomerClientResponse>(getCurrentCustomerClientRequest);

 } else {

 result = Promise.resolve({ canceled: true, data: new GetCustomerClientResponse(null) });

}
```

<span data-ttu-id="affd1-132">**強制無効トランザクション**</span><span class="sxs-lookup"><span data-stu-id="affd1-132">**Force void transaction**</span></span>
```typescript
 // Force void tarnsaction.
 let forceVoidTransactionRequest: VoidTransactionOperationRequest<VoidTransactionOperationResponse> =

 new VoidTransactionOperationRequest<VoidTransactionOperationResponse>(false, this.context.logger.getNewCorrelationId());

 this.context.runtime.executeAsync(forceVoidTransactionRequest).then((value: ICancelableDataResult<VoidTransactionOperationResponse>) => {

 this.currentCart(JSON.stringify(value.data.cart));

 }).catch((err: any) => {

 this.currentCart(JSON.stringify(err));

 });
```

### <a name="cart"></a><span data-ttu-id="affd1-133">カート</span><span class="sxs-lookup"><span data-stu-id="affd1-133">Cart</span></span>

<span data-ttu-id="affd1-134">次に、買い物カゴに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-134">The following is a list of APIs exposed to perform cart-related functionality.</span></span>

| <span data-ttu-id="affd1-135">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-135">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="affd1-136">AddPreprocessedTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-136">AddPreprocessedTenderLineToCartClientRequest</span></span>    |
| <span data-ttu-id="affd1-137">AddTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-137">AddTenderLineToCartClientRequest</span></span>                |
| <span data-ttu-id="affd1-138">ConcludeTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-138">ConcludeTransactionClientRequest</span></span>                |
| <span data-ttu-id="affd1-139">GetCurrentCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-139">GetCurrentCartClientRequest</span></span>                     |
| <span data-ttu-id="affd1-140">GetCurrentCartClientResponse</span><span class="sxs-lookup"><span data-stu-id="affd1-140">GetCurrentCartClientResponse</span></span>                    |
| <span data-ttu-id="affd1-141">GetKeyedInPriceClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-141">GetKeyedInPriceClientRequest</span></span>                    |
| <span data-ttu-id="affd1-142">GetPickupDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-142">GetPickupDateClientRequest</span></span>                      |
| <span data-ttu-id="affd1-143">GetReasonCodeLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-143">GetReasonCodeLinesClientRequest</span></span>                 |
| <span data-ttu-id="affd1-144">GetReceiptEmailAddressClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-144">GetReceiptEmailAddressClientRequest</span></span>             |
| <span data-ttu-id="affd1-145">GetShippingDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-145">GetShippingDateClientRequest</span></span>                    |
| <span data-ttu-id="affd1-146">RefreshCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-146">RefreshCartClientRequest</span></span>                        |
| <span data-ttu-id="affd1-147">ResumeSuspendedCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-147">ResumeSuspendedCartClientRequest</span></span>                |
| <span data-ttu-id="affd1-148">SaveAttributesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-148">SaveAttributesOnCartClientRequest</span></span>               |
| <span data-ttu-id="affd1-149">SaveAttributesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-149">SaveAttributesOnCartLinesClientRequest</span></span>          |
| <span data-ttu-id="affd1-150">SaveExtensionPropertiesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-150">SaveExtensionPropertiesOnCartClientRequest</span></span>      |
| <span data-ttu-id="affd1-151">SaveExtensionPropertiesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-151">SaveExtensionPropertiesOnCartLinesClientRequest</span></span> |
| <span data-ttu-id="affd1-152">SaveReasonCodeLinesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-152">SaveReasonCodeLinesOnCartClientRequest</span></span>          |
| <span data-ttu-id="affd1-153">SaveReasonCodeLinesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-153">SaveReasonCodeLinesOnCartLinesClientRequest</span></span>     |
| <span data-ttu-id="affd1-154">SelectSalesLinesForPickUpClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-154">SelectSalesLinesForPickUpClientRequest</span></span>          |
| <span data-ttu-id="affd1-155">SetCartAttributesClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-155">SetCartAttributesClientRequest</span></span>                  |
| <span data-ttu-id="affd1-156">ShowChangeDueClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-156">ShowChangeDueClientRequest</span></span>                      |
| <span data-ttu-id="affd1-157">AddAffiliationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-157">AddAffiliationOperationRequest</span></span>                  |
| <span data-ttu-id="affd1-158">AddItemToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-158">AddItemToCartOperationRequest</span></span>                   |
| <span data-ttu-id="affd1-159">CalculateTotalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-159">CalculateTotalOperationRequest</span></span>                  |
| <span data-ttu-id="affd1-160">ChangeCartLineUnitOfMeasureOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-160">ChangeCartLineUnitOfMeasureOperationRequest</span></span>     |
| <span data-ttu-id="affd1-161">CreateCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-161">CreateCustomerOrderOperationRequest</span></span>             |
| <span data-ttu-id="affd1-162">CreateCustomerQuoteOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-162">CreateCustomerQuoteOperationRequest</span></span>             |
| <span data-ttu-id="affd1-163">CustomerAccountDepositOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-163">CustomerAccountDepositOperationRequest</span></span>          |
| <span data-ttu-id="affd1-164">DepositOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-164">DepositOverrideOperationRequest</span></span>                 |
| <span data-ttu-id="affd1-165">EditCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-165">EditCustomerOrderOperationRequest</span></span>               |
| <span data-ttu-id="affd1-166">LineDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-166">LineDiscountAmountOperationRequest</span></span>              |
| <span data-ttu-id="affd1-167">LineDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-167">LineDiscountPercentOperationRequest</span></span>             |
| <span data-ttu-id="affd1-168">OverrideLineTaxFromListOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-168">OverrideLineTaxFromListOperationRequest</span></span>         |
| <span data-ttu-id="affd1-169">OverrideLineTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-169">OverrideLineTaxOperationRequest</span></span>                 |
| <span data-ttu-id="affd1-170">OverrideTransactionTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-170">OverrideTransactionTaxOperationRequest</span></span>          |
| <span data-ttu-id="affd1-171">PickupAllOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-171">PickupAllOperationRequest</span></span>                       |
| <span data-ttu-id="affd1-172">PriceOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-172">PriceOverrideOperationRequest</span></span>                   |
| <span data-ttu-id="affd1-173">SetCartLineCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-173">SetCartLineCommentOperationRequest</span></span>              |
| <span data-ttu-id="affd1-174">SetCartLineQuantityOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-174">SetCartLineQuantityOperationRequest</span></span>             |
| <span data-ttu-id="affd1-175">SetCustomerOnCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-175">SetCustomerOnCartOperationRequest</span></span>               |
| <span data-ttu-id="affd1-176">SetTransactionCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-176">SetTransactionCommentOperationRequest</span></span>           |
| <span data-ttu-id="affd1-177">SuspendCurrentCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-177">SuspendCurrentCartOperationRequest</span></span>              |
| <span data-ttu-id="affd1-178">TotalDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-178">TotalDiscountAmountOperationRequest</span></span>             |
| <span data-ttu-id="affd1-179">TotalDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-179">TotalDiscountPercentOperationRequest</span></span>            |
| <span data-ttu-id="affd1-180">VoidCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-180">VoidCartLineOperationRequest</span></span>                    |
| <span data-ttu-id="affd1-181">VoidTenderLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-181">VoidTenderLineOperationRequest</span></span>                  |
| <span data-ttu-id="affd1-182">VoidTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-182">VoidTransactionOperationRequest</span></span>                 |
| <span data-ttu-id="affd1-183">CreateEmptyCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-183">CreateEmptyCartServiceRequest</span></span>                   |
| <span data-ttu-id="affd1-184">GetTaxOverridesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-184">GetTaxOverridesServiceRequest</span></span>                   |
| <span data-ttu-id="affd1-185">UpdateTenderLineSignatureServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-185">UpdateTenderLineSignatureServiceRequest</span></span>         |
| <span data-ttu-id="affd1-186">CarryoutSelectedProductsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-186">CarryoutSelectedProductsOperationRequest</span></span> |
| <span data-ttu-id="affd1-187">AddCouponsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-187">AddCouponsOperationRequest</span></span> |
| <span data-ttu-id="affd1-188">CreateNonSalesTransactionServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-188">CreateNonSalesTransactionServiceRequest</span></span> |
| <span data-ttu-id="affd1-189">ReturnTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-189">ReturnTransactionOperationRequest</span></span> |
| <span data-ttu-id="affd1-190">AddLoyaltyCardToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-190">AddLoyaltyCardToCartOperationRequest</span></span> |
| <span data-ttu-id="affd1-191">ReturnCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-191">ReturnCartLineOperationRequest</span></span> |
| <span data-ttu-id="affd1-192">ReturnItemOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-192">ReturnItemOperationRequest</span></span> |
| <span data-ttu-id="affd1-193">AddExpenseAccountLineToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-193">AddExpenseAccountLineToCartOperationRequest</span></span> |
| <span data-ttu-id="affd1-194">ShipAllCartLinesOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-194">ShipAllCartLinesOperationRequest</span></span> |
| <span data-ttu-id="affd1-195">ShipSelectedCartLinesOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-195">ShipSelectedCartLinesOperationRequest</span></span> |


### <a name="payments"></a><span data-ttu-id="affd1-196">支払利息</span><span class="sxs-lookup"><span data-stu-id="affd1-196">Payments</span></span>

<span data-ttu-id="affd1-197">次に、支払に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-197">The following is a list of APIs exposed to perform payment-related functionality.</span></span>

| <span data-ttu-id="affd1-198">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-198">POS API</span></span>                                   | <span data-ttu-id="affd1-199">説明</span><span class="sxs-lookup"><span data-stu-id="affd1-199">Description</span></span>                            | <span data-ttu-id="affd1-200">リリース</span><span class="sxs-lookup"><span data-stu-id="affd1-200">Release</span></span>                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| <span data-ttu-id="affd1-201">GetGiftCardByIdServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-201">GetGiftCardByIdServiceRequest</span></span>             |                                        |                          |
| <span data-ttu-id="affd1-202">GetPaymentCardTypeByBinRangeClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-202">GetPaymentCardTypeByBinRangeClientRequest</span></span> |                                        |                          |
| <span data-ttu-id="affd1-203">GetSignatureClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-203">GetSignatureClientRequest</span></span>                 | <span data-ttu-id="affd1-204">署名のキャプチャ ダイアログを POS で表示するか、コンフィギュレーションに基づいてメッセージを署名キャプチャ デバイスに送信します。</span><span class="sxs-lookup"><span data-stu-id="affd1-204">Shows the signature capture dialog in POS or send the message to signature capture device based on the configuration.</span></span> | <span data-ttu-id="affd1-205">10.0.15</span><span class="sxs-lookup"><span data-stu-id="affd1-205">10.0.15</span></span> |

### <a name="peripherals"></a><span data-ttu-id="affd1-206">周辺機器</span><span class="sxs-lookup"><span data-stu-id="affd1-206">Peripherals</span></span>

<span data-ttu-id="affd1-207">次に、周辺機器に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-207">The following is a list of APIs exposed to perform peripheral-related functionality.</span></span>

| <span data-ttu-id="affd1-208">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-208">POS API</span></span>                                                |
|--------------------------------------------------------|
| <span data-ttu-id="affd1-209">CardPaymentAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-209">CardPaymentAuthorizePaymentRequest</span></span>                     |
| <span data-ttu-id="affd1-210">CardPaymentBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-210">CardPaymentBeginTransactionRequest</span></span>                     |
| <span data-ttu-id="affd1-211">CardPaymentCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-211">CardPaymentCapturePaymentRequest</span></span>                       |
| <span data-ttu-id="affd1-212">CardPaymentEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-212">CardPaymentEndTransactionRequest</span></span>                       |
| <span data-ttu-id="affd1-213">CardPaymentEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-213">CardPaymentEnquireGiftCardBalancePeripheralRequest</span></span>     |
| <span data-ttu-id="affd1-214">CardPaymentExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-214">CardPaymentExecuteTaskRequest</span></span>                          |
| <span data-ttu-id="affd1-215">CardPaymentRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-215">CardPaymentRefundPaymentRequest</span></span>                        |
| <span data-ttu-id="affd1-216">CardPaymentVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-216">CardPaymentVoidPaymentRequest</span></span>                          |
| <span data-ttu-id="affd1-217">CardPaymentAuthorizeCardTokenPeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-217">CardPaymentAuthorizeCardTokenPeripheralRequest</span></span>                          |
| <span data-ttu-id="affd1-218">CashDrawerIsOpenRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-218">CashDrawerIsOpenRequest</span></span>                                |
| <span data-ttu-id="affd1-219">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-219">HardwareStationDeviceActionRequest</span></span>                     |
| <span data-ttu-id="affd1-220">HardwareStationStatusRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-220">HardwareStationStatusRequest</span></span>                           |
| <span data-ttu-id="affd1-221">LineDisplayDisplayLinesRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-221">LineDisplayDisplayLinesRequest</span></span>                         |
| <span data-ttu-id="affd1-222">PaymentTerminalAuthorizePaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-222">PaymentTerminalAuthorizePaymentActivityRequest</span></span>         |
| <span data-ttu-id="affd1-223">PaymentTerminalAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-223">PaymentTerminalAuthorizePaymentRequest</span></span>                 |
| <span data-ttu-id="affd1-224">PaymentTerminalBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-224">PaymentTerminalBeginTransactionRequest</span></span>                 |
| <span data-ttu-id="affd1-225">PaymentTerminalCancelOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-225">PaymentTerminalCancelOperationRequest</span></span>                  |
| <span data-ttu-id="affd1-226">PaymentTerminalCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-226">PaymentTerminalCapturePaymentRequest</span></span>                   |
| <span data-ttu-id="affd1-227">PaymentTerminalEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-227">PaymentTerminalEndTransactionRequest</span></span>                   |
| <span data-ttu-id="affd1-228">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-228">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span></span> |
| <span data-ttu-id="affd1-229">PaymentTerminalExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-229">PaymentTerminalExecuteTaskRequest</span></span>                      |
| <span data-ttu-id="affd1-230">PaymentTerminalRefundPaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-230">PaymentTerminalRefundPaymentActivityRequest</span></span>            |
| <span data-ttu-id="affd1-231">PaymentTerminalRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-231">PaymentTerminalRefundPaymentRequest</span></span>                    |
| <span data-ttu-id="affd1-232">PaymentTerminalUpdateLinesRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-232">PaymentTerminalUpdateLinesRequest</span></span>                      |
| <span data-ttu-id="affd1-233">PaymentTerminalVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-233">PaymentTerminalVoidPaymentRequest</span></span>                      |
| <span data-ttu-id="affd1-234">PaymentTerminalFetchTokenPeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-234">PaymentTerminalFetchTokenPeripheralRequest</span></span>             |
| <span data-ttu-id="affd1-235">PrinterPrintRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-235">PrinterPrintRequest</span></span>                                    |
| <span data-ttu-id="affd1-236">ScaleReadRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-236">ScaleReadRequest</span></span>                                       |

### <a name="scanresults"></a><span data-ttu-id="affd1-237">ScanResults</span><span class="sxs-lookup"><span data-stu-id="affd1-237">ScanResults</span></span>

<span data-ttu-id="affd1-238">次に、スキャン結果に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-238">The following is a list of APIs exposed to perform scan results-related functionality.</span></span>

| <span data-ttu-id="affd1-239">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-239">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="affd1-240">GetScanResultClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-240">GetScanResultClientRequest</span></span> |

### <a name="customer"></a><span data-ttu-id="affd1-241">顧客</span><span class="sxs-lookup"><span data-stu-id="affd1-241">Customer</span></span>

<span data-ttu-id="affd1-242">次に、顧客に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-242">The following is a list of APIs exposed to perform customer-related functionality.</span></span>

| <span data-ttu-id="affd1-243">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-243">POS API</span></span>                  |
|--------------------------|
| <span data-ttu-id="affd1-244">GetCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-244">GetCustomerClientRequest</span></span> |
|<span data-ttu-id="affd1-245">CreateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-245">CreateCustomerServiceRequest</span></span> |
|<span data-ttu-id="affd1-246">UpdateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-246">UpdateCustomerServiceRequest</span></span> |
|<span data-ttu-id="affd1-247">SelectCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-247">SelectCustomerClientRequest</span></span> |


### <a name="authentication"></a><span data-ttu-id="affd1-248">認証</span><span class="sxs-lookup"><span data-stu-id="affd1-248">Authentication</span></span>

<span data-ttu-id="affd1-249">次に、認証に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-249">The following is a list of APIs exposed to perform authentication-related functionality.</span></span>

| <span data-ttu-id="affd1-250">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-250">POS API</span></span>                |
|------------------------|
| <span data-ttu-id="affd1-251">LogOffOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-251">LogOffOperationRequest</span></span> |
| <span data-ttu-id="affd1-252">LockRegisterOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-252">LockRegisterOperationRequest</span></span> |

### <a name="dataservice"></a><span data-ttu-id="affd1-253">DataService</span><span class="sxs-lookup"><span data-stu-id="affd1-253">DataService</span></span>

<span data-ttu-id="affd1-254">次に、データ サービスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-254">The following is a list of APIs exposed to perform data service-related functionality.</span></span>

| <span data-ttu-id="affd1-255">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-255">POS API</span></span>            |
|--------------------|
| <span data-ttu-id="affd1-256">DataServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-256">DataServiceRequest</span></span> |

### <a name="device"></a><span data-ttu-id="affd1-257">デバイス</span><span class="sxs-lookup"><span data-stu-id="affd1-257">Device</span></span>

<span data-ttu-id="affd1-258">次に、デバイスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-258">The following is a list of APIs exposed to perform device-related functionality.</span></span>

| <span data-ttu-id="affd1-259">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-259">POS API</span></span>                               |
|---------------------------------------|
| <span data-ttu-id="affd1-260">GetDeviceConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-260">GetDeviceConfigurationClientRequest</span></span>   |
| <span data-ttu-id="affd1-261">GetExtensionProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-261">GetExtensionProfileClientRequest</span></span>      |
| <span data-ttu-id="affd1-262">GetHardwareProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-262">GetHardwareProfileClientRequest</span></span>       |
| <span data-ttu-id="affd1-263">GetAuthenticationTokenClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-263">GetAuthenticationTokenClientRequest</span></span>   |
| <span data-ttu-id="affd1-264">GetConnectionStatusClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-264">GetConnectionStatusClientRequest</span></span>      |
| <span data-ttu-id="affd1-265">GetActiveHardwareStationClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-265">GetActiveHardwareStationClientRequest</span></span> |
| <span data-ttu-id="affd1-266">GetApplicationVersionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-266">GetApplicationVersionClientRequest</span></span>    |
| <span data-ttu-id="affd1-267">GetChannelConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-267">GetChannelConfigurationClientRequest</span></span>  |

### <a name="diagnostics"></a><span data-ttu-id="affd1-268">診断</span><span class="sxs-lookup"><span data-stu-id="affd1-268">Diagnostics</span></span> 

<span data-ttu-id="affd1-269">次に、診断に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-269">The following is a list of APIs exposed to perform diagnostics-related functionality.</span></span>

| <span data-ttu-id="affd1-270">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-270">POS API</span></span>                     |
|-----------------------------|
| <span data-ttu-id="affd1-271">GetSessionInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-271">GetSessionInfoClientRequest</span></span> |

### <a name="dialog"></a><span data-ttu-id="affd1-272">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="affd1-272">Dialog</span></span>

<span data-ttu-id="affd1-273">次に、ダイアログに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-273">The following is a list of APIs exposed to perform dialog-related functionality.</span></span>

| <span data-ttu-id="affd1-274">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-274">POS API</span></span>                                  |
|------------------------------------------|
| <span data-ttu-id="affd1-275">ShowMessageDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-275">ShowMessageDialogClientRequest</span></span>           |
| <span data-ttu-id="affd1-276">IAlphanumericInputDialogResult</span><span class="sxs-lookup"><span data-stu-id="affd1-276">IAlphanumericInputDialogResult</span></span>           |
| <span data-ttu-id="affd1-277">ShowAlphanumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-277">ShowAlphanumericInputDialogClientRequest</span></span> |
| <span data-ttu-id="affd1-278">ShowNumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-278">ShowNumericInputDialogClientRequest</span></span>      |
| <span data-ttu-id="affd1-279">ShowListInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-279">ShowListInputDialogClientRequest</span></span>         |
| <span data-ttu-id="affd1-280">ShowTextInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-280">ShowTextInputDialogClientRequest</span></span>         |

### <a name="employee"></a><span data-ttu-id="affd1-281">従業員</span><span class="sxs-lookup"><span data-stu-id="affd1-281">Employee</span></span>

<span data-ttu-id="affd1-282">次に、従業員に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-282">The following is a list of APIs exposed to perform employee-related functionality.</span></span>

| <span data-ttu-id="affd1-283">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-283">POS API</span></span>                          |
|----------------------------------|
| <span data-ttu-id="affd1-284">GetLoggedOnEmployeeClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-284">GetLoggedOnEmployeeClientRequest</span></span> |

### <a name="formatters"></a><span data-ttu-id="affd1-285">フォーマッター</span><span class="sxs-lookup"><span data-stu-id="affd1-285">Formatters</span></span>

<span data-ttu-id="affd1-286">次に、フォーマッターに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-286">The following is a list of APIs exposed to perform formatter-related functionality.</span></span>

| <span data-ttu-id="affd1-287">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-287">POS API</span></span>                             |
|-------------------------------------|
| <span data-ttu-id="affd1-288">IBooleanFormatter</span><span class="sxs-lookup"><span data-stu-id="affd1-288">IBooleanFormatter</span></span>                   |
| <span data-ttu-id="affd1-289">ICurrencyFormatter</span><span class="sxs-lookup"><span data-stu-id="affd1-289">ICurrencyFormatter</span></span>                  |
| <span data-ttu-id="affd1-290">IDateFormatter</span><span class="sxs-lookup"><span data-stu-id="affd1-290">IDateFormatter</span></span>                      |
| <span data-ttu-id="affd1-291">ITransactionTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="affd1-291">ITransactionTypeFormatter</span></span>           |
| <span data-ttu-id="affd1-292">IPurchaseTransferOrderTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="affd1-292">IPurchaseTransferOrderTypeFormatter</span></span> |

### <a name="orgunits"></a><span data-ttu-id="affd1-293">OrgUnits</span><span class="sxs-lookup"><span data-stu-id="affd1-293">OrgUnits</span></span>

<span data-ttu-id="affd1-294">次に、組織単位に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-294">The following is a list of APIs exposed to perform org units-related functionality.</span></span>

| <span data-ttu-id="affd1-295">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-295">POS API</span></span>                              |
|--------------------------------------|
| <span data-ttu-id="affd1-296">GetOrgUnitConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-296">GetOrgUnitConfigurationClientRequest</span></span> |
| <span data-ttu-id="affd1-297">GetOrgUnitTenderTypesClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-297">GetOrgUnitTenderTypesClientRequest</span></span>   |
| <span data-ttu-id="affd1-298">InventoryLookupOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-298">InventoryLookupOperationRequest</span></span>      |

### <a name="products"></a><span data-ttu-id="affd1-299">製品</span><span class="sxs-lookup"><span data-stu-id="affd1-299">Products</span></span>

<span data-ttu-id="affd1-300">次に、製品に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-300">The following is a list of APIs exposed to perform products-related functionality.</span></span>

| <span data-ttu-id="affd1-301">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-301">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="affd1-302">GetProductsByIdsClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-302">GetProductsByIdsClientRequest</span></span>              |
| <span data-ttu-id="affd1-303">GetCurrentProductCatalogStoreClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-303">GetCurrentProductCatalogStoreClientRequest</span></span> |
| <span data-ttu-id="affd1-304">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-304">SelectProductVariantClientRequest</span></span>          |
| <span data-ttu-id="affd1-305">GetSerialNumberClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-305">GetSerialNumberClientRequest</span></span>               |
| <span data-ttu-id="affd1-306">GetRefinerValuesByTextServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-306">GetRefinerValuesByTextServiceRequest</span></span>       |
| <span data-ttu-id="affd1-307">SelectProductClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-307">SelectProductClientRequest</span></span> |
| <span data-ttu-id="affd1-308">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-308">SelectProductVariantClientRequest</span></span> |
| <span data-ttu-id="affd1-309">GetActivePricesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-309">GetActivePricesServiceRequest</span></span> |

### <a name="categories"></a><span data-ttu-id="affd1-310">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="affd1-310">Categories</span></span>

<span data-ttu-id="affd1-311">以下は、カテゴリに関連する機能を実行する公開されている API の一覧です。</span><span class="sxs-lookup"><span data-stu-id="affd1-311">The following is a list of APIs exposed to perform categories-related functionality.</span></span>

| <span data-ttu-id="affd1-312">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-312">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="affd1-313">GetCategoriesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-313">GetCategoriesServiceRequest</span></span>              |


### <a name="salesorders"></a><span data-ttu-id="affd1-314">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="affd1-314">SalesOrders</span></span>

<span data-ttu-id="affd1-315">次に、販売注文に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-315">The following is a list of APIs exposed to perform sales orders-related functionality.</span></span>

| <span data-ttu-id="affd1-316">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-316">POS API</span></span>                                          |
|--------------------------------------------------|
| <span data-ttu-id="affd1-317">GetReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-317">GetReceiptsClientRequest</span></span>                         |
| <span data-ttu-id="affd1-318">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-318">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="affd1-319">GetSalesOrderDetailsByTransactionIdClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-319">GetSalesOrderDetailsByTransactionIdClientRequest</span></span> |
| <span data-ttu-id="affd1-320">GetGiftReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-320">GetGiftReceiptsClientRequest</span></span>                     |
| <span data-ttu-id="affd1-321">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-321">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="affd1-322">MarkAsPickedServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-322">MarkAsPickedServiceRequest</span></span>                       |
| <span data-ttu-id="affd1-323">PrintPackingSlipClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-323">PrintPackingSlipClientRequest</span></span>                    |
| <span data-ttu-id="affd1-324">PickUpCustomerOrderLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-324">PickUpCustomerOrderLinesClientRequest</span></span>            |


### <a name="shifts"></a><span data-ttu-id="affd1-325">シフト</span><span class="sxs-lookup"><span data-stu-id="affd1-325">Shifts</span></span>

<span data-ttu-id="affd1-326">次に、シフトに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-326">The following is a list of APIs exposed to perform shifts-related functionality.</span></span>

| <span data-ttu-id="affd1-327">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-327">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="affd1-328">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-328">CloseShiftOperationRequest</span></span> |
| <span data-ttu-id="affd1-329">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-329">CloseShiftOperationRequest</span></span> |

### <a name="stockcountjournals"></a><span data-ttu-id="affd1-330">StockCountJournals</span><span class="sxs-lookup"><span data-stu-id="affd1-330">StockCountJournals</span></span>

<span data-ttu-id="affd1-331">次に、在庫数仕訳帳に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-331">The following is a list of APIs exposed to perform stock count journals-related functionality.</span></span>

| <span data-ttu-id="affd1-332">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-332">POS API</span></span>                                |
|----------------------------------------|
| <span data-ttu-id="affd1-333">SyncAllStockCountJournalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-333">SyncAllStockCountJournalsClientRequest</span></span> |

### <a name="storeoperations"></a><span data-ttu-id="affd1-334">StoreOperations</span><span class="sxs-lookup"><span data-stu-id="affd1-334">StoreOperations</span></span>

<span data-ttu-id="affd1-335">次に、店舗運営に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="affd1-335">The following is a list of APIs exposed to perform store operations-related functionality.</span></span>

| <span data-ttu-id="affd1-336">POS API</span><span class="sxs-lookup"><span data-stu-id="affd1-336">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="affd1-337">DeclareStartingAmountClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-337">DeclareStartingAmountClientRequest</span></span>              |
| <span data-ttu-id="affd1-338">GetSalesOrdersWithNoFiscalTransactionsRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-338">GetSalesOrdersWithNoFiscalTransactionsRequest</span></span>   |
| <span data-ttu-id="affd1-339">RegisterCustomAuditEventClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-339">RegisterCustomAuditEventClientRequest</span></span>           |
| <span data-ttu-id="affd1-340">GetOfflinePendingTransactionCountClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-340">GetOfflinePendingTransactionCountClientRequest</span></span>  |
| <span data-ttu-id="affd1-341">SaveFiscalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-341">SaveFiscalTransactionClientRequest</span></span>              |
| <span data-ttu-id="affd1-342">SafeDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-342">SafeDropOperationRequest</span></span>                        |
| <span data-ttu-id="affd1-343">TenderDeclarationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-343">TenderDeclarationOperationRequest</span></span>               |
| <span data-ttu-id="affd1-344">TenderRemovalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-344">TenderRemovalOperationRequest</span></span>                   |
| <span data-ttu-id="affd1-345">CreateBankDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-345">CreateBankDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="affd1-346">CreateFloatEntryTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-346">CreateFloatEntryTransactionClientRequest</span></span>        |
| <span data-ttu-id="affd1-347">CreateStartingAmountTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-347">CreateStartingAmountTransactionClientRequest</span></span>    |
| <span data-ttu-id="affd1-348">CreateTenderDeclarationTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-348">CreateTenderDeclarationTransactionClientRequest</span></span> |
| <span data-ttu-id="affd1-349">CreateTenderRemovalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-349">CreateTenderRemovalTransactionClientRequest</span></span>     |
| <span data-ttu-id="affd1-350">GetDenominationTotalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-350">GetDenominationTotalsClientRequest</span></span>              |
| <span data-ttu-id="affd1-351">SelectZipCodeInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-351">SelectZipCodeInfoClientRequest</span></span>                  |
| <span data-ttu-id="affd1-352">CreateSafeDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-352">CreateSafeDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="affd1-353">GetTenderDetailsClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-353">GetTenderDetailsClientRequest</span></span>                   |
| <span data-ttu-id="affd1-354">LoyaltyCardPointsBalanceOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-354">LoyaltyCardPointsBalanceOperationRequest</span></span>        |
| <span data-ttu-id="affd1-355">GetCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-355">GetCommissionSalesGroupsServiceRequest</span></span>          |
| <span data-ttu-id="affd1-356">GetCurrenciesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-356">GetCurrenciesServiceRequest</span></span>                     |
| <span data-ttu-id="affd1-357">GetSrsReportDataSetServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-357">GetSrsReportDataSetServiceRequest</span></span>               |
| <span data-ttu-id="affd1-358">SearchCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-358">SearchCommissionSalesGroupsServiceRequest</span></span>       |
| <span data-ttu-id="affd1-359">IssueLoyaltyCardOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-359">IssueLoyaltyCardOperationRequest</span></span>                |
| <span data-ttu-id="affd1-360">GetPickingAndReceivingOrdersClientRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-360">GetPickingAndReceivingOrdersClientRequest</span></span>       |
| <span data-ttu-id="affd1-361">BankDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-361">BankDropOperationRequest</span></span>                 |
| <span data-ttu-id="affd1-362">DeclareStartAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="affd1-362">DeclareStartAmountOperationRequest</span></span>        | 


