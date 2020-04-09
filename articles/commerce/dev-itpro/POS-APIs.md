---
title: 販売時点管理 (POS) API
description: このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。
author: mugunthanm
manager: AnnBe
ms.date: 03/24/2020
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
ms.openlocfilehash: c75a33a2b71b2ab9672b8dc503b44d4be9764a12
ms.sourcegitcommit: 61f9e15c5791d27db392d0a90cd781aa8e5baa6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/24/2020
ms.locfileid: "3164710"
---
# <a name="point-of-sale-pos-apis"></a><span data-ttu-id="af5d7-103">販売時点管理 (POS) API</span><span class="sxs-lookup"><span data-stu-id="af5d7-103">Point of sale (POS) APIs</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="af5d7-104">Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-104">Retail POS APIs help you to easily build extensions or new features to the POS app.</span></span> <span data-ttu-id="af5d7-105">たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。</span><span class="sxs-lookup"><span data-stu-id="af5d7-105">For example, if you are extending the Retail POS application to add new features in which to want to get product details, change prices, or add items to a cart.</span></span> <span data-ttu-id="af5d7-106">これを実現する API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-106">you can consume APIs that will do the work for you.</span></span> <span data-ttu-id="af5d7-107">これを行うには、作業を実行する API を呼び出す必要があるだけです。</span><span class="sxs-lookup"><span data-stu-id="af5d7-107">To do this, you need to simply call the APIs to do the work.</span></span> <span data-ttu-id="af5d7-108">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-108">The POS API simplifies the extension pattern and provides continuous support to build the extensions.</span></span>

<span data-ttu-id="af5d7-109">拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。</span><span class="sxs-lookup"><span data-stu-id="af5d7-109">Extension patterns have been unified across commerce runtime (CRT), POS, and Hardware station (HWS) by following the request/response pattern.</span></span> <span data-ttu-id="af5d7-110">すべての POS API は、CRT や HWS のような要求/応答として公開されます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-110">All the POS APIs are exposed as request/response like CRT and HWS.</span></span> 

<span data-ttu-id="af5d7-111">POS API は、3 つのさまざまなシナリオに分類されます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-111">POS APIs are categorized into three different scenarios:</span></span>

- <span data-ttu-id="af5d7-112">**消費** - 拡張機能のパブリック API を使用します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-112">**Consume** – Consume public APIs in your extension.</span></span>

- <span data-ttu-id="af5d7-113">**拡張** - 一部の追加ロジックを実行するパブリック API をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="af5d7-113">**Extend** – Override public APIs to do some additional logic.</span></span>

- <span data-ttu-id="af5d7-114">**作成** - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-114">**Create** – Create new APIs using the exposed POS interface, which can be used across extensions.</span></span>

<span data-ttu-id="af5d7-115">API の多くは、拡張機能で消費できます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-115">Many APIs can be consumed in extensions.</span></span> <span data-ttu-id="af5d7-116">たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-116">For example, if you want to change the price of the item based on an external web service call, you can call PriceOverrideOperationRequest to change the price of the item.</span></span> <span data-ttu-id="af5d7-117">消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-117">Within the consume, the APIs are sub categorized by module like cart, peripherals, store operations, etc.</span></span>

> [!NOTE]
> <span data-ttu-id="af5d7-118">すべての API の一覧は、**Pos.Api.d.ts** にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。</span><span class="sxs-lookup"><span data-stu-id="af5d7-118">A list of the all of the APIs is available in **Pos.Api.d.ts**, which is part of the Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts).</span></span> <span data-ttu-id="af5d7-119">拡張機能は、公開されている要求と、POS.Api.d.ts からの応答のみを使用する必要があり、Pos.Api.d.ts を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="af5d7-119">Extensions must consume only the exposed request and response from the POS.Api.d.ts and no modification is allowed to Pos.Api.d.ts.</span></span> <span data-ttu-id="af5d7-120">拡張機能は、POS API、プロパティ、メソッド、またはハンドラーを、POS Commerce またはセッション オブジェクトから直接使用したり更新したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="af5d7-120">Extensions should not consume or update any POS APIs, properties, methods, or handlers directly from POS commerce or sessions objects.</span></span> 

## <a name="how-to-consume-apis-in-your-extension"></a><span data-ttu-id="af5d7-121">拡張機能で API を使用する方法</span><span class="sxs-lookup"><span data-stu-id="af5d7-121">How to consume APIs in your extension</span></span>

<span data-ttu-id="af5d7-122">拡張機能で Retail API を利用するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-122">Use the following steps to consume Retail APIs in your extensions.</span></span>

1.  <span data-ttu-id="af5d7-123">拡張機能ファイルで API をインポートします。</span><span class="sxs-lookup"><span data-stu-id="af5d7-123">Import the API in your extension file.</span></span>

    <span data-ttu-id="af5d7-124">たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af5d7-124">For example, if you want to consume the save attribute on cart API in your extension, then you need to add the following import statements.</span></span>

    <span data-ttu-id="af5d7-125">パターンは、"PosApi/Consume/Module name" からの {api name} のインポートです。</span><span class="sxs-lookup"><span data-stu-id="af5d7-125">The pattern is import { api name } from "PosApi/Consume/Module name";</span></span>
 
    ```typescript
    import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
    ```

2.  <span data-ttu-id="af5d7-126">必要な場合は、クライアントのエンティティとプロキシ エンティティをインポートします。</span><span class="sxs-lookup"><span data-stu-id="af5d7-126">Import the client entities and proxy entities if required.</span></span>

    ```typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
    ```
3.  <span data-ttu-id="af5d7-127">API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="af5d7-127">Declare the API variable and execute it using the POS runtime, which you can access the runtime by using: this.context.runtime.executeAsync("api name")</span></span>

    ```typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
    ```
    
    <span data-ttu-id="af5d7-128">たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="af5d7-128">For example, if you want to execute the tender removal, use SaveAttributesOnCartClientRequest api, and refer to the following steps.</span></span>
 
    ```typescript
    let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();

     attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;

     attributeValue.TextValue = "Yes";

     let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];

     let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =

    new SaveAttributesOnCartClientRequest(attributeValues);

    result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
    ```

### <a name="samples-showing-how-to-access-apis"></a><span data-ttu-id="af5d7-129">API にアクセスする方法を示すサンプル</span><span class="sxs-lookup"><span data-stu-id="af5d7-129">Samples showing how to access APIs</span></span>

<span data-ttu-id="af5d7-130">**現在の買い物カゴを取得**</span><span class="sxs-lookup"><span data-stu-id="af5d7-130">**Get Current cart**</span></span>
```typescript
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```

<span data-ttu-id="af5d7-131">**買い物カゴに追加された現在の顧客を取得**</span><span class="sxs-lookup"><span data-stu-id="af5d7-131">**Get Current customer added to cart**</span></span>
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

<span data-ttu-id="af5d7-132">**強制無効トランザクション**</span><span class="sxs-lookup"><span data-stu-id="af5d7-132">**Force void transaction**</span></span>
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

### <a name="cart"></a><span data-ttu-id="af5d7-133">カート</span><span class="sxs-lookup"><span data-stu-id="af5d7-133">Cart</span></span>

<span data-ttu-id="af5d7-134">次に、買い物カゴに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-134">The following is a list of APIs exposed to perform cart-related functionality.</span></span>

| <span data-ttu-id="af5d7-135">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-135">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="af5d7-136">AddPreprocessedTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-136">AddPreprocessedTenderLineToCartClientRequest</span></span>    |
| <span data-ttu-id="af5d7-137">AddTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-137">AddTenderLineToCartClientRequest</span></span>                |
| <span data-ttu-id="af5d7-138">ConcludeTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-138">ConcludeTransactionClientRequest</span></span>                |
| <span data-ttu-id="af5d7-139">GetCurrentCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-139">GetCurrentCartClientRequest</span></span>                     |
| <span data-ttu-id="af5d7-140">GetCurrentCartClientResponse</span><span class="sxs-lookup"><span data-stu-id="af5d7-140">GetCurrentCartClientResponse</span></span>                    |
| <span data-ttu-id="af5d7-141">GetKeyedInPriceClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-141">GetKeyedInPriceClientRequest</span></span>                    |
| <span data-ttu-id="af5d7-142">GetPickupDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-142">GetPickupDateClientRequest</span></span>                      |
| <span data-ttu-id="af5d7-143">GetReasonCodeLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-143">GetReasonCodeLinesClientRequest</span></span>                 |
| <span data-ttu-id="af5d7-144">GetReceiptEmailAddressClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-144">GetReceiptEmailAddressClientRequest</span></span>             |
| <span data-ttu-id="af5d7-145">GetShippingDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-145">GetShippingDateClientRequest</span></span>                    |
| <span data-ttu-id="af5d7-146">RefreshCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-146">RefreshCartClientRequest</span></span>                        |
| <span data-ttu-id="af5d7-147">ResumeSuspendedCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-147">ResumeSuspendedCartClientRequest</span></span>                |
| <span data-ttu-id="af5d7-148">SaveAttributesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-148">SaveAttributesOnCartClientRequest</span></span>               |
| <span data-ttu-id="af5d7-149">SaveAttributesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-149">SaveAttributesOnCartLinesClientRequest</span></span>          |
| <span data-ttu-id="af5d7-150">SaveExtensionPropertiesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-150">SaveExtensionPropertiesOnCartClientRequest</span></span>      |
| <span data-ttu-id="af5d7-151">SaveExtensionPropertiesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-151">SaveExtensionPropertiesOnCartLinesClientRequest</span></span> |
| <span data-ttu-id="af5d7-152">SaveReasonCodeLinesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-152">SaveReasonCodeLinesOnCartClientRequest</span></span>          |
| <span data-ttu-id="af5d7-153">SaveReasonCodeLinesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-153">SaveReasonCodeLinesOnCartLinesClientRequest</span></span>     |
| <span data-ttu-id="af5d7-154">SelectSalesLinesForPickUpClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-154">SelectSalesLinesForPickUpClientRequest</span></span>          |
| <span data-ttu-id="af5d7-155">SetCartAttributesClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-155">SetCartAttributesClientRequest</span></span>                  |
| <span data-ttu-id="af5d7-156">ShowChangeDueClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-156">ShowChangeDueClientRequest</span></span>                      |
| <span data-ttu-id="af5d7-157">AddAffiliationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-157">AddAffiliationOperationRequest</span></span>                  |
| <span data-ttu-id="af5d7-158">AddItemToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-158">AddItemToCartOperationRequest</span></span>                   |
| <span data-ttu-id="af5d7-159">CalculateTotalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-159">CalculateTotalOperationRequest</span></span>                  |
| <span data-ttu-id="af5d7-160">ChangeCartLineUnitOfMeasureOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-160">ChangeCartLineUnitOfMeasureOperationRequest</span></span>     |
| <span data-ttu-id="af5d7-161">CreateCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-161">CreateCustomerOrderOperationRequest</span></span>             |
| <span data-ttu-id="af5d7-162">CreateCustomerQuoteOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-162">CreateCustomerQuoteOperationRequest</span></span>             |
| <span data-ttu-id="af5d7-163">CustomerAccountDepositOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-163">CustomerAccountDepositOperationRequest</span></span>          |
| <span data-ttu-id="af5d7-164">DepositOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-164">DepositOverrideOperationRequest</span></span>                 |
| <span data-ttu-id="af5d7-165">EditCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-165">EditCustomerOrderOperationRequest</span></span>               |
| <span data-ttu-id="af5d7-166">LineDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-166">LineDiscountAmountOperationRequest</span></span>              |
| <span data-ttu-id="af5d7-167">LineDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-167">LineDiscountPercentOperationRequest</span></span>             |
| <span data-ttu-id="af5d7-168">OverrideLineTaxFromListOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-168">OverrideLineTaxFromListOperationRequest</span></span>         |
| <span data-ttu-id="af5d7-169">OverrideLineTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-169">OverrideLineTaxOperationRequest</span></span>                 |
| <span data-ttu-id="af5d7-170">OverrideTransactionTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-170">OverrideTransactionTaxOperationRequest</span></span>          |
| <span data-ttu-id="af5d7-171">PickupAllOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-171">PickupAllOperationRequest</span></span>                       |
| <span data-ttu-id="af5d7-172">PriceOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-172">PriceOverrideOperationRequest</span></span>                   |
| <span data-ttu-id="af5d7-173">SetCartLineCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-173">SetCartLineCommentOperationRequest</span></span>              |
| <span data-ttu-id="af5d7-174">SetCartLineQuantityOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-174">SetCartLineQuantityOperationRequest</span></span>             |
| <span data-ttu-id="af5d7-175">SetCustomerOnCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-175">SetCustomerOnCartOperationRequest</span></span>               |
| <span data-ttu-id="af5d7-176">SetTransactionCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-176">SetTransactionCommentOperationRequest</span></span>           |
| <span data-ttu-id="af5d7-177">SuspendCurrentCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-177">SuspendCurrentCartOperationRequest</span></span>              |
| <span data-ttu-id="af5d7-178">TotalDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-178">TotalDiscountAmountOperationRequest</span></span>             |
| <span data-ttu-id="af5d7-179">TotalDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-179">TotalDiscountPercentOperationRequest</span></span>            |
| <span data-ttu-id="af5d7-180">VoidCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-180">VoidCartLineOperationRequest</span></span>                    |
| <span data-ttu-id="af5d7-181">VoidTenderLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-181">VoidTenderLineOperationRequest</span></span>                  |
| <span data-ttu-id="af5d7-182">VoidTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-182">VoidTransactionOperationRequest</span></span>                 |
| <span data-ttu-id="af5d7-183">CreateEmptyCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-183">CreateEmptyCartServiceRequest</span></span>                   |
| <span data-ttu-id="af5d7-184">GetTaxOverridesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-184">GetTaxOverridesServiceRequest</span></span>                   |
| <span data-ttu-id="af5d7-185">UpdateTenderLineSignatureServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-185">UpdateTenderLineSignatureServiceRequest</span></span>         |
| <span data-ttu-id="af5d7-186">CarryoutSelectedProductsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-186">CarryoutSelectedProductsOperationRequest</span></span> |
| <span data-ttu-id="af5d7-187">AddCouponsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-187">AddCouponsOperationRequest</span></span> |
| <span data-ttu-id="af5d7-188">CreateNonSalesTransactionServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-188">CreateNonSalesTransactionServiceRequest</span></span> |
| <span data-ttu-id="af5d7-189">ReturnTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-189">ReturnTransactionOperationRequest</span></span> |
| <span data-ttu-id="af5d7-190">AddLoyaltyCardToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-190">AddLoyaltyCardToCartOperationRequest</span></span> |
| <span data-ttu-id="af5d7-191">ReturnCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-191">ReturnCartLineOperationRequest</span></span> |
| <span data-ttu-id="af5d7-192">ReturnItemOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-192">ReturnItemOperationRequest</span></span> |
| <span data-ttu-id="af5d7-193">AddExpenseAccountLineToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-193">AddExpenseAccountLineToCartOperationRequest</span></span> |


### <a name="payments"></a><span data-ttu-id="af5d7-194">支払利息</span><span class="sxs-lookup"><span data-stu-id="af5d7-194">Payments</span></span>

<span data-ttu-id="af5d7-195">次に、支払に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-195">The following is a list of APIs exposed to perform payment-related functionality.</span></span>

| <span data-ttu-id="af5d7-196">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-196">POS API</span></span>                                   |
|-------------------------------------------|
| <span data-ttu-id="af5d7-197">GetGiftCardByIdServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-197">GetGiftCardByIdServiceRequest</span></span>             |
| <span data-ttu-id="af5d7-198">GetPaymentCardTypeByBinRangeClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-198">GetPaymentCardTypeByBinRangeClientRequest</span></span> |

### <a name="peripherals"></a><span data-ttu-id="af5d7-199">周辺機器</span><span class="sxs-lookup"><span data-stu-id="af5d7-199">Peripherals</span></span>

<span data-ttu-id="af5d7-200">次に、周辺機器に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-200">The following is a list of APIs exposed to perform peripheral-related functionality.</span></span>

| <span data-ttu-id="af5d7-201">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-201">POS API</span></span>                                                |
|--------------------------------------------------------|
| <span data-ttu-id="af5d7-202">CardPaymentAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-202">CardPaymentAuthorizePaymentRequest</span></span>                     |
| <span data-ttu-id="af5d7-203">CardPaymentBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-203">CardPaymentBeginTransactionRequest</span></span>                     |
| <span data-ttu-id="af5d7-204">CardPaymentCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-204">CardPaymentCapturePaymentRequest</span></span>                       |
| <span data-ttu-id="af5d7-205">CardPaymentEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-205">CardPaymentEndTransactionRequest</span></span>                       |
| <span data-ttu-id="af5d7-206">CardPaymentEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-206">CardPaymentEnquireGiftCardBalancePeripheralRequest</span></span>     |
| <span data-ttu-id="af5d7-207">CardPaymentExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-207">CardPaymentExecuteTaskRequest</span></span>                          |
| <span data-ttu-id="af5d7-208">CardPaymentRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-208">CardPaymentRefundPaymentRequest</span></span>                        |
| <span data-ttu-id="af5d7-209">CardPaymentVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-209">CardPaymentVoidPaymentRequest</span></span>                          |
| <span data-ttu-id="af5d7-210">CashDrawerIsOpenRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-210">CashDrawerIsOpenRequest</span></span>                                |
| <span data-ttu-id="af5d7-211">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-211">HardwareStationDeviceActionRequest</span></span>                     |
| <span data-ttu-id="af5d7-212">HardwareStationStatusRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-212">HardwareStationStatusRequest</span></span>                           |
| <span data-ttu-id="af5d7-213">LineDisplayDisplayLinesRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-213">LineDisplayDisplayLinesRequest</span></span>                         |
| <span data-ttu-id="af5d7-214">PaymentTerminalAuthorizePaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-214">PaymentTerminalAuthorizePaymentActivityRequest</span></span>         |
| <span data-ttu-id="af5d7-215">PaymentTerminalAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-215">PaymentTerminalAuthorizePaymentRequest</span></span>                 |
| <span data-ttu-id="af5d7-216">PaymentTerminalBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-216">PaymentTerminalBeginTransactionRequest</span></span>                 |
| <span data-ttu-id="af5d7-217">PaymentTerminalCancelOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-217">PaymentTerminalCancelOperationRequest</span></span>                  |
| <span data-ttu-id="af5d7-218">PaymentTerminalCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-218">PaymentTerminalCapturePaymentRequest</span></span>                   |
| <span data-ttu-id="af5d7-219">PaymentTerminalEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-219">PaymentTerminalEndTransactionRequest</span></span>                   |
| <span data-ttu-id="af5d7-220">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-220">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span></span> |
| <span data-ttu-id="af5d7-221">PaymentTerminalExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-221">PaymentTerminalExecuteTaskRequest</span></span>                      |
| <span data-ttu-id="af5d7-222">PaymentTerminalRefundPaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-222">PaymentTerminalRefundPaymentActivityRequest</span></span>            |
| <span data-ttu-id="af5d7-223">PaymentTerminalRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-223">PaymentTerminalRefundPaymentRequest</span></span>                    |
| <span data-ttu-id="af5d7-224">PaymentTerminalUpdateLinesRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-224">PaymentTerminalUpdateLinesRequest</span></span>                      |
| <span data-ttu-id="af5d7-225">PaymentTerminalVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-225">PaymentTerminalVoidPaymentRequest</span></span>                      |
| <span data-ttu-id="af5d7-226">PrinterPrintRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-226">PrinterPrintRequest</span></span>                                    |
| <span data-ttu-id="af5d7-227">ScaleReadRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-227">ScaleReadRequest</span></span>                                       |

### <a name="scanresults"></a><span data-ttu-id="af5d7-228">ScanResults</span><span class="sxs-lookup"><span data-stu-id="af5d7-228">ScanResults</span></span>

<span data-ttu-id="af5d7-229">次に、スキャン結果に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-229">The following is a list of APIs exposed to perform scan results-related functionality.</span></span>

| <span data-ttu-id="af5d7-230">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-230">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="af5d7-231">GetScanResultClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-231">GetScanResultClientRequest</span></span> |

### <a name="customer"></a><span data-ttu-id="af5d7-232">顧客</span><span class="sxs-lookup"><span data-stu-id="af5d7-232">Customer</span></span>

<span data-ttu-id="af5d7-233">次に、顧客に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-233">The following is a list of APIs exposed to perform customer-related functionality.</span></span>

| <span data-ttu-id="af5d7-234">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-234">POS API</span></span>                  |
|--------------------------|
| <span data-ttu-id="af5d7-235">GetCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-235">GetCustomerClientRequest</span></span> |
|<span data-ttu-id="af5d7-236">CreateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-236">CreateCustomerServiceRequest</span></span> |
|<span data-ttu-id="af5d7-237">UpdateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-237">UpdateCustomerServiceRequest</span></span> |
|<span data-ttu-id="af5d7-238">SelectCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-238">SelectCustomerClientRequest</span></span> |


### <a name="authentication"></a><span data-ttu-id="af5d7-239">認証</span><span class="sxs-lookup"><span data-stu-id="af5d7-239">Authentication</span></span>

<span data-ttu-id="af5d7-240">次に、認証に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-240">The following is a list of APIs exposed to perform authentication-related functionality.</span></span>

| <span data-ttu-id="af5d7-241">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-241">POS API</span></span>                |
|------------------------|
| <span data-ttu-id="af5d7-242">LogOffOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-242">LogOffOperationRequest</span></span> |

### <a name="dataservice"></a><span data-ttu-id="af5d7-243">DataService</span><span class="sxs-lookup"><span data-stu-id="af5d7-243">DataService</span></span>

<span data-ttu-id="af5d7-244">次に、データ サービスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-244">The following is a list of APIs exposed to perform data service-related functionality.</span></span>

| <span data-ttu-id="af5d7-245">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-245">POS API</span></span>            |
|--------------------|
| <span data-ttu-id="af5d7-246">DataServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-246">DataServiceRequest</span></span> |

### <a name="device"></a><span data-ttu-id="af5d7-247">デバイス</span><span class="sxs-lookup"><span data-stu-id="af5d7-247">Device</span></span>

<span data-ttu-id="af5d7-248">次に、デバイスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-248">The following is a list of APIs exposed to perform device-related functionality.</span></span>

| <span data-ttu-id="af5d7-249">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-249">POS API</span></span>                               |
|---------------------------------------|
| <span data-ttu-id="af5d7-250">GetDeviceConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-250">GetDeviceConfigurationClientRequest</span></span>   |
| <span data-ttu-id="af5d7-251">GetExtensionProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-251">GetExtensionProfileClientRequest</span></span>      |
| <span data-ttu-id="af5d7-252">GetHardwareProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-252">GetHardwareProfileClientRequest</span></span>       |
| <span data-ttu-id="af5d7-253">GetAuthenticationTokenClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-253">GetAuthenticationTokenClientRequest</span></span>   |
| <span data-ttu-id="af5d7-254">GetConnectionStatusClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-254">GetConnectionStatusClientRequest</span></span>      |
| <span data-ttu-id="af5d7-255">GetActiveHardwareStationClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-255">GetActiveHardwareStationClientRequest</span></span> |
| <span data-ttu-id="af5d7-256">GetApplicationVersionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-256">GetApplicationVersionClientRequest</span></span>    |
| <span data-ttu-id="af5d7-257">GetChannelConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-257">GetChannelConfigurationClientRequest</span></span>  |

### <a name="diagnostics"></a><span data-ttu-id="af5d7-258">診断</span><span class="sxs-lookup"><span data-stu-id="af5d7-258">Diagnostics</span></span> 

<span data-ttu-id="af5d7-259">次に、診断に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-259">The following is a list of APIs exposed to perform diagnostics-related functionality.</span></span>

| <span data-ttu-id="af5d7-260">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-260">POS API</span></span>                     |
|-----------------------------|
| <span data-ttu-id="af5d7-261">GetSessionInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-261">GetSessionInfoClientRequest</span></span> |

### <a name="dialog"></a><span data-ttu-id="af5d7-262">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="af5d7-262">Dialog</span></span>

<span data-ttu-id="af5d7-263">次に、ダイアログに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-263">The following is a list of APIs exposed to perform dialog-related functionality.</span></span>

| <span data-ttu-id="af5d7-264">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-264">POS API</span></span>                                  |
|------------------------------------------|
| <span data-ttu-id="af5d7-265">ShowMessageDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-265">ShowMessageDialogClientRequest</span></span>           |
| <span data-ttu-id="af5d7-266">IAlphanumericInputDialogResult</span><span class="sxs-lookup"><span data-stu-id="af5d7-266">IAlphanumericInputDialogResult</span></span>           |
| <span data-ttu-id="af5d7-267">ShowAlphanumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-267">ShowAlphanumericInputDialogClientRequest</span></span> |
| <span data-ttu-id="af5d7-268">ShowNumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-268">ShowNumericInputDialogClientRequest</span></span>      |
| <span data-ttu-id="af5d7-269">ShowListInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-269">ShowListInputDialogClientRequest</span></span>         |
| <span data-ttu-id="af5d7-270">ShowTextInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-270">ShowTextInputDialogClientRequest</span></span>         |

### <a name="employee"></a><span data-ttu-id="af5d7-271">従業員</span><span class="sxs-lookup"><span data-stu-id="af5d7-271">Employee</span></span>

<span data-ttu-id="af5d7-272">次に、従業員に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-272">The following is a list of APIs exposed to perform employee-related functionality.</span></span>

| <span data-ttu-id="af5d7-273">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-273">POS API</span></span>                          |
|----------------------------------|
| <span data-ttu-id="af5d7-274">GetLoggedOnEmployeeClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-274">GetLoggedOnEmployeeClientRequest</span></span> |

### <a name="formatters"></a><span data-ttu-id="af5d7-275">フォーマッター</span><span class="sxs-lookup"><span data-stu-id="af5d7-275">Formatters</span></span>

<span data-ttu-id="af5d7-276">次に、フォーマッターに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-276">The following is a list of APIs exposed to perform formatter-related functionality.</span></span>

| <span data-ttu-id="af5d7-277">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-277">POS API</span></span>                             |
|-------------------------------------|
| <span data-ttu-id="af5d7-278">IBooleanFormatter</span><span class="sxs-lookup"><span data-stu-id="af5d7-278">IBooleanFormatter</span></span>                   |
| <span data-ttu-id="af5d7-279">ICurrencyFormatter</span><span class="sxs-lookup"><span data-stu-id="af5d7-279">ICurrencyFormatter</span></span>                  |
| <span data-ttu-id="af5d7-280">IDateFormatter</span><span class="sxs-lookup"><span data-stu-id="af5d7-280">IDateFormatter</span></span>                      |
| <span data-ttu-id="af5d7-281">ITransactionTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="af5d7-281">ITransactionTypeFormatter</span></span>           |
| <span data-ttu-id="af5d7-282">IPurchaseTransferOrderTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="af5d7-282">IPurchaseTransferOrderTypeFormatter</span></span> |

### <a name="orgunits"></a><span data-ttu-id="af5d7-283">OrgUnits</span><span class="sxs-lookup"><span data-stu-id="af5d7-283">OrgUnits</span></span>

<span data-ttu-id="af5d7-284">次に、組織単位に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-284">The following is a list of APIs exposed to perform org units-related functionality.</span></span>

| <span data-ttu-id="af5d7-285">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-285">POS API</span></span>                              |
|--------------------------------------|
| <span data-ttu-id="af5d7-286">GetOrgUnitConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-286">GetOrgUnitConfigurationClientRequest</span></span> |
| <span data-ttu-id="af5d7-287">GetOrgUnitTenderTypesClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-287">GetOrgUnitTenderTypesClientRequest</span></span>   |
| <span data-ttu-id="af5d7-288">InventoryLookupOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-288">InventoryLookupOperationRequest</span></span>      |

### <a name="products"></a><span data-ttu-id="af5d7-289">製品</span><span class="sxs-lookup"><span data-stu-id="af5d7-289">Products</span></span>

<span data-ttu-id="af5d7-290">次に、製品に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-290">The following is a list of APIs exposed to perform products-related functionality.</span></span>

| <span data-ttu-id="af5d7-291">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-291">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="af5d7-292">GetProductsByIdsClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-292">GetProductsByIdsClientRequest</span></span>              |
| <span data-ttu-id="af5d7-293">GetCurrentProductCatalogStoreClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-293">GetCurrentProductCatalogStoreClientRequest</span></span> |
| <span data-ttu-id="af5d7-294">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-294">SelectProductVariantClientRequest</span></span>          |
| <span data-ttu-id="af5d7-295">GetSerialNumberClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-295">GetSerialNumberClientRequest</span></span>               |
| <span data-ttu-id="af5d7-296">GetRefinerValuesByTextServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-296">GetRefinerValuesByTextServiceRequest</span></span>       |
| <span data-ttu-id="af5d7-297">SelectProductClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-297">SelectProductClientRequest</span></span> |

### <a name="salesorders"></a><span data-ttu-id="af5d7-298">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="af5d7-298">SalesOrders</span></span>

<span data-ttu-id="af5d7-299">次に、販売注文に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-299">The following is a list of APIs exposed to perform sales orders-related functionality.</span></span>

| <span data-ttu-id="af5d7-300">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-300">POS API</span></span>                                          |
|--------------------------------------------------|
| <span data-ttu-id="af5d7-301">GetReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-301">GetReceiptsClientRequest</span></span>                         |
| <span data-ttu-id="af5d7-302">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-302">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="af5d7-303">GetSalesOrderDetailsByTransactionIdClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-303">GetSalesOrderDetailsByTransactionIdClientRequest</span></span> |
| <span data-ttu-id="af5d7-304">GetGiftReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-304">GetGiftReceiptsClientRequest</span></span>                     |
| <span data-ttu-id="af5d7-305">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-305">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="af5d7-306">MarkAsPickedServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-306">MarkAsPickedServiceRequest</span></span>                       |
| <span data-ttu-id="af5d7-307">PrintPackingSlipClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-307">PrintPackingSlipClientRequest</span></span>                    |
| <span data-ttu-id="af5d7-308">PickUpCustomerOrderLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-308">PickUpCustomerOrderLinesClientRequest</span></span>            |


### <a name="shifts"></a><span data-ttu-id="af5d7-309">シフト</span><span class="sxs-lookup"><span data-stu-id="af5d7-309">Shifts</span></span>

<span data-ttu-id="af5d7-310">次に、シフトに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-310">The following is a list of APIs exposed to perform shifts-related functionality.</span></span>

| <span data-ttu-id="af5d7-311">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-311">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="af5d7-312">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-312">CloseShiftOperationRequest</span></span> |
| <span data-ttu-id="af5d7-313">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-313">CloseShiftOperationRequest</span></span> |

### <a name="stockcountjournals"></a><span data-ttu-id="af5d7-314">StockCountJournals</span><span class="sxs-lookup"><span data-stu-id="af5d7-314">StockCountJournals</span></span>

<span data-ttu-id="af5d7-315">次に、在庫数仕訳帳に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-315">The following is a list of APIs exposed to perform stock count journals-related functionality.</span></span>

| <span data-ttu-id="af5d7-316">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-316">POS API</span></span>                                |
|----------------------------------------|
| <span data-ttu-id="af5d7-317">SyncAllStockCountJournalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-317">SyncAllStockCountJournalsClientRequest</span></span> |

### <a name="storeoperations"></a><span data-ttu-id="af5d7-318">StoreOperations</span><span class="sxs-lookup"><span data-stu-id="af5d7-318">StoreOperations</span></span>

<span data-ttu-id="af5d7-319">次に、店舗運営に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="af5d7-319">The following is a list of APIs exposed to perform store operations-related functionality.</span></span>

| <span data-ttu-id="af5d7-320">POS API</span><span class="sxs-lookup"><span data-stu-id="af5d7-320">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="af5d7-321">DeclareStartingAmountClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-321">DeclareStartingAmountClientRequest</span></span>              |
| <span data-ttu-id="af5d7-322">GetSalesOrdersWithNoFiscalTransactionsRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-322">GetSalesOrdersWithNoFiscalTransactionsRequest</span></span>   |
| <span data-ttu-id="af5d7-323">RegisterCustomAuditEventClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-323">RegisterCustomAuditEventClientRequest</span></span>           |
| <span data-ttu-id="af5d7-324">GetOfflinePendingTransactionCountClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-324">GetOfflinePendingTransactionCountClientRequest</span></span>  |
| <span data-ttu-id="af5d7-325">SaveFiscalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-325">SaveFiscalTransactionClientRequest</span></span>              |
| <span data-ttu-id="af5d7-326">SafeDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-326">SafeDropOperationRequest</span></span>                        |
| <span data-ttu-id="af5d7-327">TenderDeclarationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-327">TenderDeclarationOperationRequest</span></span>               |
| <span data-ttu-id="af5d7-328">TenderRemovalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-328">TenderRemovalOperationRequest</span></span>                   |
| <span data-ttu-id="af5d7-329">CreateBankDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-329">CreateBankDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="af5d7-330">CreateFloatEntryTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-330">CreateFloatEntryTransactionClientRequest</span></span>        |
| <span data-ttu-id="af5d7-331">CreateStartingAmountTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-331">CreateStartingAmountTransactionClientRequest</span></span>    |
| <span data-ttu-id="af5d7-332">CreateTenderDeclarationTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-332">CreateTenderDeclarationTransactionClientRequest</span></span> |
| <span data-ttu-id="af5d7-333">CreateTenderRemovalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-333">CreateTenderRemovalTransactionClientRequest</span></span>     |
| <span data-ttu-id="af5d7-334">GetDenominationTotalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-334">GetDenominationTotalsClientRequest</span></span>              |
| <span data-ttu-id="af5d7-335">SelectZipCodeInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-335">SelectZipCodeInfoClientRequest</span></span>                  |
| <span data-ttu-id="af5d7-336">CreateSafeDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-336">CreateSafeDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="af5d7-337">GetTenderDetailsClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-337">GetTenderDetailsClientRequest</span></span>                   |
| <span data-ttu-id="af5d7-338">LoyaltyCardPointsBalanceOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-338">LoyaltyCardPointsBalanceOperationRequest</span></span>        |
| <span data-ttu-id="af5d7-339">GetCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-339">GetCommissionSalesGroupsServiceRequest</span></span>          |
| <span data-ttu-id="af5d7-340">GetCurrenciesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-340">GetCurrenciesServiceRequest</span></span>                     |
| <span data-ttu-id="af5d7-341">GetSrsReportDataSetServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-341">GetSrsReportDataSetServiceRequest</span></span>               |
| <span data-ttu-id="af5d7-342">SearchCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-342">SearchCommissionSalesGroupsServiceRequest</span></span>       |
| <span data-ttu-id="af5d7-343">IssueLoyaltyCardOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-343">IssueLoyaltyCardOperationRequest</span></span>                |
| <span data-ttu-id="af5d7-344">GetPickingAndReceivingOrdersClientRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-344">GetPickingAndReceivingOrdersClientRequest</span></span>       |
| <span data-ttu-id="af5d7-345">BankDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-345">BankDropOperationRequest</span></span>                 |
| <span data-ttu-id="af5d7-346">DeclareStartAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="af5d7-346">DeclareStartAmountOperationRequest</span></span>        |


