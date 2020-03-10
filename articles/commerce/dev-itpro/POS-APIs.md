---
title: 販売時点管理 (POS) API
description: このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。
author: mugunthanm
manager: AnnBe
ms.date: 11/19/2019
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
ms.openlocfilehash: b043dbc93bc16571a0fcdaf4bf520d4c6de97ca6
ms.sourcegitcommit: 4359e7e4eec25362df61c9a26c7218604d12da3d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2020
ms.locfileid: "3078056"
---
# <a name="point-of-sale-pos-apis"></a><span data-ttu-id="3c79f-103">販売時点管理 (POS) API</span><span class="sxs-lookup"><span data-stu-id="3c79f-103">Point of sale (POS) APIs</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c79f-104">Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-104">Retail POS APIs help you to easily build extensions or new features to the POS app.</span></span> <span data-ttu-id="3c79f-105">たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。</span><span class="sxs-lookup"><span data-stu-id="3c79f-105">For example, if you are extending the Retail POS application to add new features in which to want to get product details, change prices, or add items to a cart.</span></span> <span data-ttu-id="3c79f-106">これを実現する API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-106">you can consume APIs that will do the work for you.</span></span> <span data-ttu-id="3c79f-107">これを行うには、作業を実行する API を呼び出す必要があるだけです。</span><span class="sxs-lookup"><span data-stu-id="3c79f-107">To do this, you need to simply call the APIs to do the work.</span></span> <span data-ttu-id="3c79f-108">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-108">The POS API simplifies the extension pattern and provides continuous support to build the extensions.</span></span>

<span data-ttu-id="3c79f-109">拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。</span><span class="sxs-lookup"><span data-stu-id="3c79f-109">Extension patterns have been unified across commerce runtime (CRT), POS, and Hardware station (HWS) by following the request/response pattern.</span></span> <span data-ttu-id="3c79f-110">すべての POS API は、CRT や HWS のような要求/応答として公開されます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-110">All the POS APIs are exposed as request/response like CRT and HWS.</span></span> 

<span data-ttu-id="3c79f-111">POS API は、3 つのさまざまなシナリオに分類されます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-111">POS APIs are categorized into three different scenarios:</span></span>

- <span data-ttu-id="3c79f-112">**消費** - 拡張機能のパブリック API を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-112">**Consume** – Consume public APIs in your extension.</span></span>

- <span data-ttu-id="3c79f-113">**拡張** - 一部の追加ロジックを実行するパブリック API をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3c79f-113">**Extend** – Override public APIs to do some additional logic.</span></span>

- <span data-ttu-id="3c79f-114">**作成** - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-114">**Create** – Create new APIs using the exposed POS interface, which can be used across extensions.</span></span>

<span data-ttu-id="3c79f-115">API の多くは、拡張機能で消費できます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-115">Many APIs can be consumed in extensions.</span></span> <span data-ttu-id="3c79f-116">たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-116">For example, if you want to change the price of the item based on an external web service call, you can call PriceOverrideOperationRequest to change the price of the item.</span></span> <span data-ttu-id="3c79f-117">消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-117">Within the consume, the APIs are sub categorized by module like cart, peripherals, store operations, etc.</span></span>

> [!NOTE]
> <span data-ttu-id="3c79f-118">すべての API の一覧は、**Pos.Api.d.ts** にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。</span><span class="sxs-lookup"><span data-stu-id="3c79f-118">A list of the all of the APIs is available in **Pos.Api.d.ts**, which is part of the Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts).</span></span> <span data-ttu-id="3c79f-119">拡張機能は、公開されている要求と、POS.Api.d.ts からの応答のみを使用する必要があり、Pos.Api.d.ts を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="3c79f-119">Extensions must consume only the exposed request and response from the POS.Api.d.ts and no modification is allowed to Pos.Api.d.ts.</span></span> <span data-ttu-id="3c79f-120">拡張機能は、POS API、プロパティ、メソッド、またはハンドラーを、POS Commerce またはセッション オブジェクトから直接使用したり更新したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="3c79f-120">Extensions should not consume or update any POS APIs, properties, methods, or handlers directly from POS commerce or sessions objects.</span></span> 

## <a name="how-to-consume-apis-in-your-extension"></a><span data-ttu-id="3c79f-121">拡張機能で API を使用する方法</span><span class="sxs-lookup"><span data-stu-id="3c79f-121">How to consume APIs in your extension</span></span>

<span data-ttu-id="3c79f-122">拡張機能で Retail API を利用するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-122">Use the following steps to consume Retail APIs in your extensions.</span></span>

1.  <span data-ttu-id="3c79f-123">拡張機能ファイルで API をインポートします。</span><span class="sxs-lookup"><span data-stu-id="3c79f-123">Import the API in your extension file.</span></span>

    <span data-ttu-id="3c79f-124">たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c79f-124">For example, if you want to consume the save attribute on cart API in your extension, then you need to add the following import statements.</span></span>

    <span data-ttu-id="3c79f-125">パターンは、"PosApi/Consume/Module name" からの {api name} のインポートです。</span><span class="sxs-lookup"><span data-stu-id="3c79f-125">The pattern is import { api name } from "PosApi/Consume/Module name";</span></span>
 
    ```typescript
    import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
    ```

2.  <span data-ttu-id="3c79f-126">必要な場合は、クライアントのエンティティとプロキシ エンティティをインポートします。</span><span class="sxs-lookup"><span data-stu-id="3c79f-126">Import the client entities and proxy entities if required.</span></span>

    ```typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
    ```
3.  <span data-ttu-id="3c79f-127">API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3c79f-127">Declare the API variable and execute it using the POS runtime, which you can access the runtime by using: this.context.runtime.executeAsync("api name")</span></span>

    ```typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
    ```
    
    <span data-ttu-id="3c79f-128">たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c79f-128">For example, if you want to execute the tender removal, use SaveAttributesOnCartClientRequest api, and refer to the following steps.</span></span>
 
    ```typescript
    let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();

     attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;

     attributeValue.TextValue = "Yes";

     let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];

     let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =

    new SaveAttributesOnCartClientRequest(attributeValues);

    result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
    ```

### <a name="samples-showing-how-to-access-apis"></a><span data-ttu-id="3c79f-129">API にアクセスする方法を示すサンプル</span><span class="sxs-lookup"><span data-stu-id="3c79f-129">Samples showing how to access APIs</span></span>

<span data-ttu-id="3c79f-130">**現在の買い物カゴを取得**</span><span class="sxs-lookup"><span data-stu-id="3c79f-130">**Get Current cart**</span></span>
```typescript
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```

<span data-ttu-id="3c79f-131">**買い物カゴに追加された現在の顧客を取得**</span><span class="sxs-lookup"><span data-stu-id="3c79f-131">**Get Current customer added to cart**</span></span>
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

<span data-ttu-id="3c79f-132">**強制無効トランザクション**</span><span class="sxs-lookup"><span data-stu-id="3c79f-132">**Force void transaction**</span></span>
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

### <a name="cart"></a><span data-ttu-id="3c79f-133">カート</span><span class="sxs-lookup"><span data-stu-id="3c79f-133">Cart</span></span>

<span data-ttu-id="3c79f-134">次に、買い物カゴに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-134">The following is a list of APIs exposed to perform cart-related functionality.</span></span>

| <span data-ttu-id="3c79f-135">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-135">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="3c79f-136">AddPreprocessedTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-136">AddPreprocessedTenderLineToCartClientRequest</span></span>    |
| <span data-ttu-id="3c79f-137">AddTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-137">AddTenderLineToCartClientRequest</span></span>                |
| <span data-ttu-id="3c79f-138">ConcludeTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-138">ConcludeTransactionClientRequest</span></span>                |
| <span data-ttu-id="3c79f-139">GetCurrentCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-139">GetCurrentCartClientRequest</span></span>                     |
| <span data-ttu-id="3c79f-140">GetCurrentCartClientResponse</span><span class="sxs-lookup"><span data-stu-id="3c79f-140">GetCurrentCartClientResponse</span></span>                    |
| <span data-ttu-id="3c79f-141">GetKeyedInPriceClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-141">GetKeyedInPriceClientRequest</span></span>                    |
| <span data-ttu-id="3c79f-142">GetPickupDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-142">GetPickupDateClientRequest</span></span>                      |
| <span data-ttu-id="3c79f-143">GetReasonCodeLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-143">GetReasonCodeLinesClientRequest</span></span>                 |
| <span data-ttu-id="3c79f-144">GetReceiptEmailAddressClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-144">GetReceiptEmailAddressClientRequest</span></span>             |
| <span data-ttu-id="3c79f-145">GetShippingDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-145">GetShippingDateClientRequest</span></span>                    |
| <span data-ttu-id="3c79f-146">RefreshCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-146">RefreshCartClientRequest</span></span>                        |
| <span data-ttu-id="3c79f-147">ResumeSuspendedCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-147">ResumeSuspendedCartClientRequest</span></span>                |
| <span data-ttu-id="3c79f-148">SaveAttributesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-148">SaveAttributesOnCartClientRequest</span></span>               |
| <span data-ttu-id="3c79f-149">SaveAttributesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-149">SaveAttributesOnCartLinesClientRequest</span></span>          |
| <span data-ttu-id="3c79f-150">SaveExtensionPropertiesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-150">SaveExtensionPropertiesOnCartClientRequest</span></span>      |
| <span data-ttu-id="3c79f-151">SaveExtensionPropertiesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-151">SaveExtensionPropertiesOnCartLinesClientRequest</span></span> |
| <span data-ttu-id="3c79f-152">SaveReasonCodeLinesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-152">SaveReasonCodeLinesOnCartClientRequest</span></span>          |
| <span data-ttu-id="3c79f-153">SaveReasonCodeLinesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-153">SaveReasonCodeLinesOnCartLinesClientRequest</span></span>     |
| <span data-ttu-id="3c79f-154">SelectSalesLinesForPickUpClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-154">SelectSalesLinesForPickUpClientRequest</span></span>          |
| <span data-ttu-id="3c79f-155">SetCartAttributesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-155">SetCartAttributesClientRequest</span></span>                  |
| <span data-ttu-id="3c79f-156">ShowChangeDueClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-156">ShowChangeDueClientRequest</span></span>                      |
| <span data-ttu-id="3c79f-157">AddAffiliationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-157">AddAffiliationOperationRequest</span></span>                  |
| <span data-ttu-id="3c79f-158">AddItemToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-158">AddItemToCartOperationRequest</span></span>                   |
| <span data-ttu-id="3c79f-159">CalculateTotalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-159">CalculateTotalOperationRequest</span></span>                  |
| <span data-ttu-id="3c79f-160">ChangeCartLineUnitOfMeasureOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-160">ChangeCartLineUnitOfMeasureOperationRequest</span></span>     |
| <span data-ttu-id="3c79f-161">CreateCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-161">CreateCustomerOrderOperationRequest</span></span>             |
| <span data-ttu-id="3c79f-162">CreateCustomerQuoteOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-162">CreateCustomerQuoteOperationRequest</span></span>             |
| <span data-ttu-id="3c79f-163">CustomerAccountDepositOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-163">CustomerAccountDepositOperationRequest</span></span>          |
| <span data-ttu-id="3c79f-164">DepositOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-164">DepositOverrideOperationRequest</span></span>                 |
| <span data-ttu-id="3c79f-165">EditCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-165">EditCustomerOrderOperationRequest</span></span>               |
| <span data-ttu-id="3c79f-166">LineDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-166">LineDiscountAmountOperationRequest</span></span>              |
| <span data-ttu-id="3c79f-167">LineDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-167">LineDiscountPercentOperationRequest</span></span>             |
| <span data-ttu-id="3c79f-168">OverrideLineTaxFromListOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-168">OverrideLineTaxFromListOperationRequest</span></span>         |
| <span data-ttu-id="3c79f-169">OverrideLineTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-169">OverrideLineTaxOperationRequest</span></span>                 |
| <span data-ttu-id="3c79f-170">OverrideTransactionTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-170">OverrideTransactionTaxOperationRequest</span></span>          |
| <span data-ttu-id="3c79f-171">PickupAllOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-171">PickupAllOperationRequest</span></span>                       |
| <span data-ttu-id="3c79f-172">PriceOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-172">PriceOverrideOperationRequest</span></span>                   |
| <span data-ttu-id="3c79f-173">SetCartLineCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-173">SetCartLineCommentOperationRequest</span></span>              |
| <span data-ttu-id="3c79f-174">SetCartLineQuantityOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-174">SetCartLineQuantityOperationRequest</span></span>             |
| <span data-ttu-id="3c79f-175">SetCustomerOnCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-175">SetCustomerOnCartOperationRequest</span></span>               |
| <span data-ttu-id="3c79f-176">SetTransactionCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-176">SetTransactionCommentOperationRequest</span></span>           |
| <span data-ttu-id="3c79f-177">SuspendCurrentCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-177">SuspendCurrentCartOperationRequest</span></span>              |
| <span data-ttu-id="3c79f-178">TotalDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-178">TotalDiscountAmountOperationRequest</span></span>             |
| <span data-ttu-id="3c79f-179">TotalDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-179">TotalDiscountPercentOperationRequest</span></span>            |
| <span data-ttu-id="3c79f-180">VoidCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-180">VoidCartLineOperationRequest</span></span>                    |
| <span data-ttu-id="3c79f-181">VoidTenderLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-181">VoidTenderLineOperationRequest</span></span>                  |
| <span data-ttu-id="3c79f-182">VoidTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-182">VoidTransactionOperationRequest</span></span>                 |
| <span data-ttu-id="3c79f-183">CreateEmptyCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-183">CreateEmptyCartServiceRequest</span></span>                   |
| <span data-ttu-id="3c79f-184">GetTaxOverridesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-184">GetTaxOverridesServiceRequest</span></span>                   |
| <span data-ttu-id="3c79f-185">UpdateTenderLineSignatureServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-185">UpdateTenderLineSignatureServiceRequest</span></span>         |
| <span data-ttu-id="3c79f-186">CarryoutSelectedProductsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-186">CarryoutSelectedProductsOperationRequest</span></span> |
| <span data-ttu-id="3c79f-187">AddCouponsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-187">AddCouponsOperationRequest</span></span> |
| <span data-ttu-id="3c79f-188">CreateNonSalesTransactionServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-188">CreateNonSalesTransactionServiceRequest</span></span> |
| <span data-ttu-id="3c79f-189">ReturnTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-189">ReturnTransactionOperationRequest</span></span> |
| <span data-ttu-id="3c79f-190">AddLoyaltyCardToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-190">AddLoyaltyCardToCartOperationRequest</span></span> |
| <span data-ttu-id="3c79f-191">ReturnCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-191">ReturnCartLineOperationRequest</span></span> |
| <span data-ttu-id="3c79f-192">ReturnItemOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-192">ReturnItemOperationRequest</span></span> |


### <a name="payments"></a><span data-ttu-id="3c79f-193">支払</span><span class="sxs-lookup"><span data-stu-id="3c79f-193">Payments</span></span>

<span data-ttu-id="3c79f-194">次に、支払に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-194">The following is a list of APIs exposed to perform payment-related functionality.</span></span>

| <span data-ttu-id="3c79f-195">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-195">POS API</span></span>                                   |
|-------------------------------------------|
| <span data-ttu-id="3c79f-196">GetGiftCardByIdServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-196">GetGiftCardByIdServiceRequest</span></span>             |
| <span data-ttu-id="3c79f-197">GetPaymentCardTypeByBinRangeClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-197">GetPaymentCardTypeByBinRangeClientRequest</span></span> |

### <a name="peripherals"></a><span data-ttu-id="3c79f-198">周辺機器</span><span class="sxs-lookup"><span data-stu-id="3c79f-198">Peripherals</span></span>

<span data-ttu-id="3c79f-199">次に、周辺機器に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-199">The following is a list of APIs exposed to perform peripheral-related functionality.</span></span>

| <span data-ttu-id="3c79f-200">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-200">POS API</span></span>                                                |
|--------------------------------------------------------|
| <span data-ttu-id="3c79f-201">CardPaymentAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-201">CardPaymentAuthorizePaymentRequest</span></span>                     |
| <span data-ttu-id="3c79f-202">CardPaymentBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-202">CardPaymentBeginTransactionRequest</span></span>                     |
| <span data-ttu-id="3c79f-203">CardPaymentCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-203">CardPaymentCapturePaymentRequest</span></span>                       |
| <span data-ttu-id="3c79f-204">CardPaymentEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-204">CardPaymentEndTransactionRequest</span></span>                       |
| <span data-ttu-id="3c79f-205">CardPaymentEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-205">CardPaymentEnquireGiftCardBalancePeripheralRequest</span></span>     |
| <span data-ttu-id="3c79f-206">CardPaymentExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-206">CardPaymentExecuteTaskRequest</span></span>                          |
| <span data-ttu-id="3c79f-207">CardPaymentRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-207">CardPaymentRefundPaymentRequest</span></span>                        |
| <span data-ttu-id="3c79f-208">CardPaymentVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-208">CardPaymentVoidPaymentRequest</span></span>                          |
| <span data-ttu-id="3c79f-209">CashDrawerIsOpenRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-209">CashDrawerIsOpenRequest</span></span>                                |
| <span data-ttu-id="3c79f-210">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-210">HardwareStationDeviceActionRequest</span></span>                     |
| <span data-ttu-id="3c79f-211">HardwareStationStatusRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-211">HardwareStationStatusRequest</span></span>                           |
| <span data-ttu-id="3c79f-212">LineDisplayDisplayLinesRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-212">LineDisplayDisplayLinesRequest</span></span>                         |
| <span data-ttu-id="3c79f-213">PaymentTerminalAuthorizePaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-213">PaymentTerminalAuthorizePaymentActivityRequest</span></span>         |
| <span data-ttu-id="3c79f-214">PaymentTerminalAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-214">PaymentTerminalAuthorizePaymentRequest</span></span>                 |
| <span data-ttu-id="3c79f-215">PaymentTerminalBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-215">PaymentTerminalBeginTransactionRequest</span></span>                 |
| <span data-ttu-id="3c79f-216">PaymentTerminalCancelOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-216">PaymentTerminalCancelOperationRequest</span></span>                  |
| <span data-ttu-id="3c79f-217">PaymentTerminalCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-217">PaymentTerminalCapturePaymentRequest</span></span>                   |
| <span data-ttu-id="3c79f-218">PaymentTerminalEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-218">PaymentTerminalEndTransactionRequest</span></span>                   |
| <span data-ttu-id="3c79f-219">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-219">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span></span> |
| <span data-ttu-id="3c79f-220">PaymentTerminalExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-220">PaymentTerminalExecuteTaskRequest</span></span>                      |
| <span data-ttu-id="3c79f-221">PaymentTerminalRefundPaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-221">PaymentTerminalRefundPaymentActivityRequest</span></span>            |
| <span data-ttu-id="3c79f-222">PaymentTerminalRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-222">PaymentTerminalRefundPaymentRequest</span></span>                    |
| <span data-ttu-id="3c79f-223">PaymentTerminalUpdateLinesRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-223">PaymentTerminalUpdateLinesRequest</span></span>                      |
| <span data-ttu-id="3c79f-224">PaymentTerminalVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-224">PaymentTerminalVoidPaymentRequest</span></span>                      |
| <span data-ttu-id="3c79f-225">PrinterPrintRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-225">PrinterPrintRequest</span></span>                                    |
| <span data-ttu-id="3c79f-226">ScaleReadRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-226">ScaleReadRequest</span></span>                                       |

### <a name="scanresults"></a><span data-ttu-id="3c79f-227">ScanResults</span><span class="sxs-lookup"><span data-stu-id="3c79f-227">ScanResults</span></span>

<span data-ttu-id="3c79f-228">次に、スキャン結果に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-228">The following is a list of APIs exposed to perform scan results-related functionality.</span></span>

| <span data-ttu-id="3c79f-229">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-229">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="3c79f-230">GetScanResultClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-230">GetScanResultClientRequest</span></span> |

### <a name="customer"></a><span data-ttu-id="3c79f-231">顧客</span><span class="sxs-lookup"><span data-stu-id="3c79f-231">Customer</span></span>

<span data-ttu-id="3c79f-232">次に、顧客に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-232">The following is a list of APIs exposed to perform customer-related functionality.</span></span>

| <span data-ttu-id="3c79f-233">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-233">POS API</span></span>                  |
|--------------------------|
| <span data-ttu-id="3c79f-234">GetCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-234">GetCustomerClientRequest</span></span> |
|<span data-ttu-id="3c79f-235">CreateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-235">CreateCustomerServiceRequest</span></span> |
|<span data-ttu-id="3c79f-236">UpdateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-236">UpdateCustomerServiceRequest</span></span> |
|<span data-ttu-id="3c79f-237">SelectCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-237">SelectCustomerClientRequest</span></span> |


### <a name="authentication"></a><span data-ttu-id="3c79f-238">認証</span><span class="sxs-lookup"><span data-stu-id="3c79f-238">Authentication</span></span>

<span data-ttu-id="3c79f-239">次に、認証に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-239">The following is a list of APIs exposed to perform authentication-related functionality.</span></span>

| <span data-ttu-id="3c79f-240">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-240">POS API</span></span>                |
|------------------------|
| <span data-ttu-id="3c79f-241">LogOffOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-241">LogOffOperationRequest</span></span> |

### <a name="dataservice"></a><span data-ttu-id="3c79f-242">DataService</span><span class="sxs-lookup"><span data-stu-id="3c79f-242">DataService</span></span>

<span data-ttu-id="3c79f-243">次に、データ サービスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-243">The following is a list of APIs exposed to perform data service-related functionality.</span></span>

| <span data-ttu-id="3c79f-244">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-244">POS API</span></span>            |
|--------------------|
| <span data-ttu-id="3c79f-245">DataServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-245">DataServiceRequest</span></span> |

### <a name="device"></a><span data-ttu-id="3c79f-246">デバイス</span><span class="sxs-lookup"><span data-stu-id="3c79f-246">Device</span></span>

<span data-ttu-id="3c79f-247">次に、デバイスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-247">The following is a list of APIs exposed to perform device-related functionality.</span></span>

| <span data-ttu-id="3c79f-248">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-248">POS API</span></span>                               |
|---------------------------------------|
| <span data-ttu-id="3c79f-249">GetDeviceConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-249">GetDeviceConfigurationClientRequest</span></span>   |
| <span data-ttu-id="3c79f-250">GetExtensionProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-250">GetExtensionProfileClientRequest</span></span>      |
| <span data-ttu-id="3c79f-251">GetHardwareProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-251">GetHardwareProfileClientRequest</span></span>       |
| <span data-ttu-id="3c79f-252">GetAuthenticationTokenClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-252">GetAuthenticationTokenClientRequest</span></span>   |
| <span data-ttu-id="3c79f-253">GetConnectionStatusClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-253">GetConnectionStatusClientRequest</span></span>      |
| <span data-ttu-id="3c79f-254">GetActiveHardwareStationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-254">GetActiveHardwareStationClientRequest</span></span> |
| <span data-ttu-id="3c79f-255">GetApplicationVersionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-255">GetApplicationVersionClientRequest</span></span>    |
| <span data-ttu-id="3c79f-256">GetChannelConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-256">GetChannelConfigurationClientRequest</span></span>  |

### <a name="diagnostics"></a><span data-ttu-id="3c79f-257">診断</span><span class="sxs-lookup"><span data-stu-id="3c79f-257">Diagnostics</span></span> 

<span data-ttu-id="3c79f-258">次に、診断に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-258">The following is a list of APIs exposed to perform diagnostics-related functionality.</span></span>

| <span data-ttu-id="3c79f-259">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-259">POS API</span></span>                     |
|-----------------------------|
| <span data-ttu-id="3c79f-260">GetSessionInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-260">GetSessionInfoClientRequest</span></span> |

### <a name="dialog"></a><span data-ttu-id="3c79f-261">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="3c79f-261">Dialog</span></span>

<span data-ttu-id="3c79f-262">次に、ダイアログに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-262">The following is a list of APIs exposed to perform dialog-related functionality.</span></span>

| <span data-ttu-id="3c79f-263">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-263">POS API</span></span>                                  |
|------------------------------------------|
| <span data-ttu-id="3c79f-264">ShowMessageDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-264">ShowMessageDialogClientRequest</span></span>           |
| <span data-ttu-id="3c79f-265">IAlphanumericInputDialogResult</span><span class="sxs-lookup"><span data-stu-id="3c79f-265">IAlphanumericInputDialogResult</span></span>           |
| <span data-ttu-id="3c79f-266">ShowAlphanumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-266">ShowAlphanumericInputDialogClientRequest</span></span> |
| <span data-ttu-id="3c79f-267">ShowNumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-267">ShowNumericInputDialogClientRequest</span></span>      |
| <span data-ttu-id="3c79f-268">ShowListInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-268">ShowListInputDialogClientRequest</span></span>         |
| <span data-ttu-id="3c79f-269">ShowTextInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-269">ShowTextInputDialogClientRequest</span></span>         |

### <a name="employee"></a><span data-ttu-id="3c79f-270">従業員</span><span class="sxs-lookup"><span data-stu-id="3c79f-270">Employee</span></span>

<span data-ttu-id="3c79f-271">次に、従業員に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-271">The following is a list of APIs exposed to perform employee-related functionality.</span></span>

| <span data-ttu-id="3c79f-272">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-272">POS API</span></span>                          |
|----------------------------------|
| <span data-ttu-id="3c79f-273">GetLoggedOnEmployeeClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-273">GetLoggedOnEmployeeClientRequest</span></span> |

### <a name="formatters"></a><span data-ttu-id="3c79f-274">フォーマッター</span><span class="sxs-lookup"><span data-stu-id="3c79f-274">Formatters</span></span>

<span data-ttu-id="3c79f-275">次に、フォーマッターに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-275">The following is a list of APIs exposed to perform formatter-related functionality.</span></span>

| <span data-ttu-id="3c79f-276">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-276">POS API</span></span>                             |
|-------------------------------------|
| <span data-ttu-id="3c79f-277">IBooleanFormatter</span><span class="sxs-lookup"><span data-stu-id="3c79f-277">IBooleanFormatter</span></span>                   |
| <span data-ttu-id="3c79f-278">ICurrencyFormatter</span><span class="sxs-lookup"><span data-stu-id="3c79f-278">ICurrencyFormatter</span></span>                  |
| <span data-ttu-id="3c79f-279">IDateFormatter</span><span class="sxs-lookup"><span data-stu-id="3c79f-279">IDateFormatter</span></span>                      |
| <span data-ttu-id="3c79f-280">ITransactionTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="3c79f-280">ITransactionTypeFormatter</span></span>           |
| <span data-ttu-id="3c79f-281">IPurchaseTransferOrderTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="3c79f-281">IPurchaseTransferOrderTypeFormatter</span></span> |

### <a name="orgunits"></a><span data-ttu-id="3c79f-282">OrgUnits</span><span class="sxs-lookup"><span data-stu-id="3c79f-282">OrgUnits</span></span>

<span data-ttu-id="3c79f-283">次に、組織単位に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-283">The following is a list of APIs exposed to perform org units-related functionality.</span></span>

| <span data-ttu-id="3c79f-284">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-284">POS API</span></span>                              |
|--------------------------------------|
| <span data-ttu-id="3c79f-285">GetOrgUnitConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-285">GetOrgUnitConfigurationClientRequest</span></span> |
| <span data-ttu-id="3c79f-286">GetOrgUnitTenderTypesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-286">GetOrgUnitTenderTypesClientRequest</span></span>   |
| <span data-ttu-id="3c79f-287">InventoryLookupOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-287">InventoryLookupOperationRequest</span></span>      |

### <a name="products"></a><span data-ttu-id="3c79f-288">製品</span><span class="sxs-lookup"><span data-stu-id="3c79f-288">Products</span></span>

<span data-ttu-id="3c79f-289">次に、製品に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-289">The following is a list of APIs exposed to perform products-related functionality.</span></span>

| <span data-ttu-id="3c79f-290">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-290">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="3c79f-291">GetProductsByIdsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-291">GetProductsByIdsClientRequest</span></span>              |
| <span data-ttu-id="3c79f-292">GetCurrentProductCatalogStoreClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-292">GetCurrentProductCatalogStoreClientRequest</span></span> |
| <span data-ttu-id="3c79f-293">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-293">SelectProductVariantClientRequest</span></span>          |
| <span data-ttu-id="3c79f-294">GetSerialNumberClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-294">GetSerialNumberClientRequest</span></span>               |
| <span data-ttu-id="3c79f-295">GetRefinerValuesByTextServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-295">GetRefinerValuesByTextServiceRequest</span></span>       |
| <span data-ttu-id="3c79f-296">SelectProductClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-296">SelectProductClientRequest</span></span> |

### <a name="salesorders"></a><span data-ttu-id="3c79f-297">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="3c79f-297">SalesOrders</span></span>

<span data-ttu-id="3c79f-298">次に、販売注文に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-298">The following is a list of APIs exposed to perform sales orders-related functionality.</span></span>

| <span data-ttu-id="3c79f-299">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-299">POS API</span></span>                                          |
|--------------------------------------------------|
| <span data-ttu-id="3c79f-300">GetReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-300">GetReceiptsClientRequest</span></span>                         |
| <span data-ttu-id="3c79f-301">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-301">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="3c79f-302">GetSalesOrderDetailsByTransactionIdClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-302">GetSalesOrderDetailsByTransactionIdClientRequest</span></span> |
| <span data-ttu-id="3c79f-303">GetGiftReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-303">GetGiftReceiptsClientRequest</span></span>                     |
| <span data-ttu-id="3c79f-304">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-304">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="3c79f-305">MarkAsPickedServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-305">MarkAsPickedServiceRequest</span></span>                       |
| <span data-ttu-id="3c79f-306">PrintPackingSlipClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-306">PrintPackingSlipClientRequest</span></span>                    |
| <span data-ttu-id="3c79f-307">PickUpCustomerOrderLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-307">PickUpCustomerOrderLinesClientRequest</span></span>            |


### <a name="shifts"></a><span data-ttu-id="3c79f-308">シフト</span><span class="sxs-lookup"><span data-stu-id="3c79f-308">Shifts</span></span>

<span data-ttu-id="3c79f-309">次に、シフトに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-309">The following is a list of APIs exposed to perform shifts-related functionality.</span></span>

| <span data-ttu-id="3c79f-310">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-310">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="3c79f-311">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-311">CloseShiftOperationRequest</span></span> |
| <span data-ttu-id="3c79f-312">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-312">CloseShiftOperationRequest</span></span> |

### <a name="stockcountjournals"></a><span data-ttu-id="3c79f-313">StockCountJournals</span><span class="sxs-lookup"><span data-stu-id="3c79f-313">StockCountJournals</span></span>

<span data-ttu-id="3c79f-314">次に、在庫数仕訳帳に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-314">The following is a list of APIs exposed to perform stock count journals-related functionality.</span></span>

| <span data-ttu-id="3c79f-315">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-315">POS API</span></span>                                |
|----------------------------------------|
| <span data-ttu-id="3c79f-316">SyncAllStockCountJournalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-316">SyncAllStockCountJournalsClientRequest</span></span> |

### <a name="storeoperations"></a><span data-ttu-id="3c79f-317">StoreOperations</span><span class="sxs-lookup"><span data-stu-id="3c79f-317">StoreOperations</span></span>

<span data-ttu-id="3c79f-318">次に、店舗運営に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3c79f-318">The following is a list of APIs exposed to perform store operations-related functionality.</span></span>

| <span data-ttu-id="3c79f-319">POS API</span><span class="sxs-lookup"><span data-stu-id="3c79f-319">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="3c79f-320">DeclareStartingAmountClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-320">DeclareStartingAmountClientRequest</span></span>              |
| <span data-ttu-id="3c79f-321">GetSalesOrdersWithNoFiscalTransactionsRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-321">GetSalesOrdersWithNoFiscalTransactionsRequest</span></span>   |
| <span data-ttu-id="3c79f-322">RegisterCustomAuditEventClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-322">RegisterCustomAuditEventClientRequest</span></span>           |
| <span data-ttu-id="3c79f-323">GetOfflinePendingTransactionCountClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-323">GetOfflinePendingTransactionCountClientRequest</span></span>  |
| <span data-ttu-id="3c79f-324">SaveFiscalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-324">SaveFiscalTransactionClientRequest</span></span>              |
| <span data-ttu-id="3c79f-325">SafeDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-325">SafeDropOperationRequest</span></span>                        |
| <span data-ttu-id="3c79f-326">TenderDeclarationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-326">TenderDeclarationOperationRequest</span></span>               |
| <span data-ttu-id="3c79f-327">TenderRemovalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-327">TenderRemovalOperationRequest</span></span>                   |
| <span data-ttu-id="3c79f-328">CreateBankDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-328">CreateBankDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="3c79f-329">CreateFloatEntryTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-329">CreateFloatEntryTransactionClientRequest</span></span>        |
| <span data-ttu-id="3c79f-330">CreateStartingAmountTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-330">CreateStartingAmountTransactionClientRequest</span></span>    |
| <span data-ttu-id="3c79f-331">CreateTenderDeclarationTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-331">CreateTenderDeclarationTransactionClientRequest</span></span> |
| <span data-ttu-id="3c79f-332">CreateTenderRemovalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-332">CreateTenderRemovalTransactionClientRequest</span></span>     |
| <span data-ttu-id="3c79f-333">GetDenominationTotalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-333">GetDenominationTotalsClientRequest</span></span>              |
| <span data-ttu-id="3c79f-334">SelectZipCodeInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-334">SelectZipCodeInfoClientRequest</span></span>                  |
| <span data-ttu-id="3c79f-335">CreateSafeDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-335">CreateSafeDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="3c79f-336">GetTenderDetailsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-336">GetTenderDetailsClientRequest</span></span>                   |
| <span data-ttu-id="3c79f-337">LoyaltyCardPointsBalanceOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-337">LoyaltyCardPointsBalanceOperationRequest</span></span>        |
| <span data-ttu-id="3c79f-338">GetCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-338">GetCommissionSalesGroupsServiceRequest</span></span>          |
| <span data-ttu-id="3c79f-339">GetCurrenciesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-339">GetCurrenciesServiceRequest</span></span>                     |
| <span data-ttu-id="3c79f-340">GetSrsReportDataSetServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-340">GetSrsReportDataSetServiceRequest</span></span>               |
| <span data-ttu-id="3c79f-341">SearchCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-341">SearchCommissionSalesGroupsServiceRequest</span></span>       |
| <span data-ttu-id="3c79f-342">IssueLoyaltyCardOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-342">IssueLoyaltyCardOperationRequest</span></span>                |
| <span data-ttu-id="3c79f-343">GetPickingAndReceivingOrdersClientRequest</span><span class="sxs-lookup"><span data-stu-id="3c79f-343">GetPickingAndReceivingOrdersClientRequest</span></span>       |


