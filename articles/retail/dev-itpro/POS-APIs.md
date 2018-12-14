---
title: Retail POS API
description: "このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。"
author: mugunthanm
manager: AnnBe
ms.date: 12/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-29-10
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: 4fe430afe625328ce212fd2f72e836585f920490
ms.openlocfilehash: e126c65837f4057a3ace0cf5e4c877a41c82d784
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="retail-pos-apis"></a><span data-ttu-id="06265-103">Retail POS API</span><span class="sxs-lookup"><span data-stu-id="06265-103">Retail POS APIs</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="06265-104">Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="06265-104">Retail POS APIs help you to easily build extensions or new features to the POS app.</span></span> <span data-ttu-id="06265-105">たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。</span><span class="sxs-lookup"><span data-stu-id="06265-105">For example, if you are extending the Retail POS application to add new features in which to want to get product details, change prices, or add items to a cart.</span></span> <span data-ttu-id="06265-106">これを実現する API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="06265-106">you can consume APIs that will do the work for you.</span></span> <span data-ttu-id="06265-107">これを行うには、作業を実行する API を呼び出す必要があるだけです。</span><span class="sxs-lookup"><span data-stu-id="06265-107">To do this, you need to simply call the APIs to do the work.</span></span> <span data-ttu-id="06265-108">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="06265-108">The POS API simplifies the extension pattern and provides continuous support to build the extensions.</span></span>

<span data-ttu-id="06265-109">拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。</span><span class="sxs-lookup"><span data-stu-id="06265-109">Extension patterns have been unified across commerce runtime (CRT), POS, and Hardware station (HWS) by following the request/response pattern.</span></span> <span data-ttu-id="06265-110">すべての POS API は、CRT や HWS のような要求/応答として公開されます。</span><span class="sxs-lookup"><span data-stu-id="06265-110">All the POS APIs are exposed as request/response like CRT and HWS.</span></span> <span data-ttu-id="06265-111">このトピックは、最新の修正プログラムが適用された Dynamics 365 for Finance and Operations または Dynamics 365 for Retail に適用されます。</span><span class="sxs-lookup"><span data-stu-id="06265-111">This topic is applicable for Dynamics 365 for Finance and Operations or Dynamics 365 for Retail with the latest hotfix.</span></span> 

<span data-ttu-id="06265-112">POS API は、3 つのさまざまなシナリオに分類されます。</span><span class="sxs-lookup"><span data-stu-id="06265-112">POS APIs are categorized into three different scenarios:</span></span>

- <span data-ttu-id="06265-113">**消費** - 拡張機能のパブリック API を使用します。</span><span class="sxs-lookup"><span data-stu-id="06265-113">**Consume** – Consume public APIs in your extension.</span></span>

- <span data-ttu-id="06265-114">**拡張** - 一部の追加ロジックを実行するパブリック API をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="06265-114">**Extend** – Override public APIs to do some additional logic.</span></span>

- <span data-ttu-id="06265-115">**作成** - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="06265-115">**Create** – Create new APIs using the exposed POS interface, which can be used across extensions.</span></span>

<span data-ttu-id="06265-116">API の多くは、拡張機能で消費できます。</span><span class="sxs-lookup"><span data-stu-id="06265-116">Many APIs can be consumed in extensions.</span></span> <span data-ttu-id="06265-117">たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="06265-117">For example, if you want to change the price of the item based on an external web service call, you can call PriceOverrideOperationRequest to change the price of the item.</span></span> <span data-ttu-id="06265-118">消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。</span><span class="sxs-lookup"><span data-stu-id="06265-118">Within the consume, the APIs are sub categorized by module like cart, peripherals, store operations, etc.</span></span>

> [!NOTE]
> <span data-ttu-id="06265-119">すべての API の一覧は、**Pos.Api.d.ts** にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。</span><span class="sxs-lookup"><span data-stu-id="06265-119">A list of the all of the APIs is available in **Pos.Api.d.ts**, which is part of the Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts).</span></span> <span data-ttu-id="06265-120">拡張機能は、公開されている要求と、POS.Api.d.ts からの応答のみを使用する必要があり、Pos.Api.d.ts を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="06265-120">Extensions must consume only the exposed request and response from the POS.Api.d.ts and no modification is allowed to Pos.Api.d.ts.</span></span> <span data-ttu-id="06265-121">拡張機能は、POS API、プロパティ、メソッド、またはハンドラーを、POS Commerce またはセッション オブジェクトから直接使用したり更新したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="06265-121">Extensions should not consume or update any POS APIs, properties, methods, or handlers directly from POS commerce or sessions objects.</span></span> 

## <a name="how-to-consume-apis-in-your-extension"></a><span data-ttu-id="06265-122">拡張機能で API を使用する方法</span><span class="sxs-lookup"><span data-stu-id="06265-122">How to consume APIs in your extension</span></span>

<span data-ttu-id="06265-123">拡張機能で Retail API を利用するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="06265-123">Use the following steps to consume Retail APIs in your extensions.</span></span>

1.  <span data-ttu-id="06265-124">拡張機能ファイルで API をインポートします。</span><span class="sxs-lookup"><span data-stu-id="06265-124">Import the API in your extension file.</span></span>

    <span data-ttu-id="06265-125">たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06265-125">For example, if you want to consume the save attribute on cart API in your extension, then you need to add the following import statements.</span></span>

 <span data-ttu-id="06265-126">パターンは、"PosApi/Consume/Module name"; からの { API 名 } のインポートです</span><span class="sxs-lookup"><span data-stu-id="06265-126">The pattern is import { api name } from "PosApi/Consume/Module name";</span></span>
```Typescript
 import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
```

2.  <span data-ttu-id="06265-127">必要な場合は、クライアントのエンティティとプロキシ エンティティをインポートします。</span><span class="sxs-lookup"><span data-stu-id="06265-127">Import the client entities and proxy entities if required.</span></span>

```Typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
```
3.  <span data-ttu-id="06265-128">API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="06265-128">Declare the API variable and execute it using the POS runtime, which you can access the runtime by using: this.context.runtime.executeAsync("api name")</span></span>

```Typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
```

 <span data-ttu-id="06265-129">たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06265-129">For example, if you want to execute the tender removal, use SaveAttributesOnCartClientRequest api, and refer to the following steps.</span></span>
```Typescript
let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();

 attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;

 attributeValue.TextValue = "Yes";

 let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];

 let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =

new SaveAttributesOnCartClientRequest(attributeValues);

result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);

```
### <a name="samples-showing-how-to-access-apis"></a><span data-ttu-id="06265-130">API にアクセスする方法を示すサンプル</span><span class="sxs-lookup"><span data-stu-id="06265-130">Samples showing how to access APIs</span></span>

<span data-ttu-id="06265-131">**現在の買い物カゴを取得**</span><span class="sxs-lookup"><span data-stu-id="06265-131">**Get Current cart**</span></span>
```
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```
<span data-ttu-id="06265-132">**買い物カゴに追加された現在の顧客を取得**</span><span class="sxs-lookup"><span data-stu-id="06265-132">**Get Current customer added to cart**</span></span>
```
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
<span data-ttu-id="06265-133">**強制無効トランザクション**</span><span class="sxs-lookup"><span data-stu-id="06265-133">**Force void transaction**</span></span>
```
 // Force void tarnsaction.
```Typescript
 let forceVoidTransactionRequest: VoidTransactionOperationRequest<VoidTransactionOperationResponse> =

 new VoidTransactionOperationRequest<VoidTransactionOperationResponse>(false, this.context.logger.getNewCorrelationId());

 this.context.runtime.executeAsync(forceVoidTransactionRequest).then((value: ICancelableDataResult<VoidTransactionOperationResponse>) => {

 this.currentCart(JSON.stringify(value.data.cart));

 }).catch((err: any) => {

 this.currentCart(JSON.stringify(err));

 });
```

### <a name="cart"></a><span data-ttu-id="06265-134">カート</span><span class="sxs-lookup"><span data-stu-id="06265-134">Cart</span></span>

<span data-ttu-id="06265-135">次に、買い物カゴに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-135">The following is a list of APIs exposed to perform cart-related functionality.</span></span>

| <span data-ttu-id="06265-136">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-136">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="06265-137">AddPreprocessedTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-137">AddPreprocessedTenderLineToCartClientRequest</span></span>    |
| <span data-ttu-id="06265-138">AddTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-138">AddTenderLineToCartClientRequest</span></span>                |
| <span data-ttu-id="06265-139">ConcludeTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-139">ConcludeTransactionClientRequest</span></span>                |
| <span data-ttu-id="06265-140">GetCurrentCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-140">GetCurrentCartClientRequest</span></span>                     |
| <span data-ttu-id="06265-141">GetCurrentCartClientResponse</span><span class="sxs-lookup"><span data-stu-id="06265-141">GetCurrentCartClientResponse</span></span>                    |
| <span data-ttu-id="06265-142">GetKeyedInPriceClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-142">GetKeyedInPriceClientRequest</span></span>                    |
| <span data-ttu-id="06265-143">GetPickupDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-143">GetPickupDateClientRequest</span></span>                      |
| <span data-ttu-id="06265-144">GetReasonCodeLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-144">GetReasonCodeLinesClientRequest</span></span>                 |
| <span data-ttu-id="06265-145">GetReceiptEmailAddressClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-145">GetReceiptEmailAddressClientRequest</span></span>             |
| <span data-ttu-id="06265-146">GetShippingDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-146">GetShippingDateClientRequest</span></span>                    |
| <span data-ttu-id="06265-147">RefreshCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-147">RefreshCartClientRequest</span></span>                        |
| <span data-ttu-id="06265-148">ResumeSuspendedCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-148">ResumeSuspendedCartClientRequest</span></span>                |
| <span data-ttu-id="06265-149">SaveAttributesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-149">SaveAttributesOnCartClientRequest</span></span>               |
| <span data-ttu-id="06265-150">SaveAttributesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-150">SaveAttributesOnCartLinesClientRequest</span></span>          |
| <span data-ttu-id="06265-151">SaveExtensionPropertiesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-151">SaveExtensionPropertiesOnCartClientRequest</span></span>      |
| <span data-ttu-id="06265-152">SaveExtensionPropertiesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-152">SaveExtensionPropertiesOnCartLinesClientRequest</span></span> |
| <span data-ttu-id="06265-153">SaveReasonCodeLinesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-153">SaveReasonCodeLinesOnCartClientRequest</span></span>          |
| <span data-ttu-id="06265-154">SaveReasonCodeLinesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-154">SaveReasonCodeLinesOnCartLinesClientRequest</span></span>     |
| <span data-ttu-id="06265-155">SelectSalesLinesForPickUpClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-155">SelectSalesLinesForPickUpClientRequest</span></span>          |
| <span data-ttu-id="06265-156">SetCartAttributesClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-156">SetCartAttributesClientRequest</span></span>                  |
| <span data-ttu-id="06265-157">ShowChangeDueClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-157">ShowChangeDueClientRequest</span></span>                      |
| <span data-ttu-id="06265-158">AddAffiliationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-158">AddAffiliationOperationRequest</span></span>                  |
| <span data-ttu-id="06265-159">AddItemToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-159">AddItemToCartOperationRequest</span></span>                   |
| <span data-ttu-id="06265-160">CalculateTotalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-160">CalculateTotalOperationRequest</span></span>                  |
| <span data-ttu-id="06265-161">ChangeCartLineUnitOfMeasureOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-161">ChangeCartLineUnitOfMeasureOperationRequest</span></span>     |
| <span data-ttu-id="06265-162">CreateCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-162">CreateCustomerOrderOperationRequest</span></span>             |
| <span data-ttu-id="06265-163">CreateCustomerQuoteOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-163">CreateCustomerQuoteOperationRequest</span></span>             |
| <span data-ttu-id="06265-164">CustomerAccountDepositOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-164">CustomerAccountDepositOperationRequest</span></span>          |
| <span data-ttu-id="06265-165">DepositOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-165">DepositOverrideOperationRequest</span></span>                 |
| <span data-ttu-id="06265-166">EditCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-166">EditCustomerOrderOperationRequest</span></span>               |
| <span data-ttu-id="06265-167">LineDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-167">LineDiscountAmountOperationRequest</span></span>              |
| <span data-ttu-id="06265-168">LineDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-168">LineDiscountPercentOperationRequest</span></span>             |
| <span data-ttu-id="06265-169">OverrideLineTaxFromListOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-169">OverrideLineTaxFromListOperationRequest</span></span>         |
| <span data-ttu-id="06265-170">OverrideLineTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-170">OverrideLineTaxOperationRequest</span></span>                 |
| <span data-ttu-id="06265-171">OverrideTransactionTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-171">OverrideTransactionTaxOperationRequest</span></span>          |
| <span data-ttu-id="06265-172">PickupAllOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-172">PickupAllOperationRequest</span></span>                       |
| <span data-ttu-id="06265-173">PriceOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-173">PriceOverrideOperationRequest</span></span>                   |
| <span data-ttu-id="06265-174">SetCartLineCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-174">SetCartLineCommentOperationRequest</span></span>              |
| <span data-ttu-id="06265-175">SetCartLineQuantityOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-175">SetCartLineQuantityOperationRequest</span></span>             |
| <span data-ttu-id="06265-176">SetCustomerOnCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-176">SetCustomerOnCartOperationRequest</span></span>               |
| <span data-ttu-id="06265-177">SetTransactionCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-177">SetTransactionCommentOperationRequest</span></span>           |
| <span data-ttu-id="06265-178">SuspendCurrentCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-178">SuspendCurrentCartOperationRequest</span></span>              |
| <span data-ttu-id="06265-179">TotalDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-179">TotalDiscountAmountOperationRequest</span></span>             |
| <span data-ttu-id="06265-180">TotalDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-180">TotalDiscountPercentOperationRequest</span></span>            |
| <span data-ttu-id="06265-181">VoidCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-181">VoidCartLineOperationRequest</span></span>                    |
| <span data-ttu-id="06265-182">VoidTenderLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-182">VoidTenderLineOperationRequest</span></span>                  |
| <span data-ttu-id="06265-183">VoidTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-183">VoidTransactionOperationRequest</span></span>                 |
| <span data-ttu-id="06265-184">CreateEmptyCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-184">CreateEmptyCartServiceRequest</span></span>                   |
| <span data-ttu-id="06265-185">GetTaxOverridesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-185">GetTaxOverridesServiceRequest</span></span>                   |
| <span data-ttu-id="06265-186">UpdateTenderLineSignatureServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-186">UpdateTenderLineSignatureServiceRequest</span></span>         |
| <span data-ttu-id="06265-187">CarryoutSelectedProductsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-187">CarryoutSelectedProductsOperationRequest</span></span> |

### <a name="payments"></a><span data-ttu-id="06265-188">支払利息</span><span class="sxs-lookup"><span data-stu-id="06265-188">Payments</span></span>

<span data-ttu-id="06265-189">次に、支払に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-189">The following is a list of APIs exposed to perform payment-related functionality.</span></span>

| <span data-ttu-id="06265-190">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-190">POS API</span></span>                                   |
|-------------------------------------------|
| <span data-ttu-id="06265-191">GetGiftCardByIdServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-191">GetGiftCardByIdServiceRequest</span></span>             |
| <span data-ttu-id="06265-192">GetPaymentCardTypeByBinRangeClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-192">GetPaymentCardTypeByBinRangeClientRequest</span></span> |

### <a name="peripherals"></a><span data-ttu-id="06265-193">周辺機器</span><span class="sxs-lookup"><span data-stu-id="06265-193">Peripherals</span></span>

<span data-ttu-id="06265-194">次に、周辺機器に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-194">The following is a list of APIs exposed to perform peripheral-related functionality.</span></span>

| <span data-ttu-id="06265-195">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-195">POS API</span></span>                                                |
|--------------------------------------------------------|
| <span data-ttu-id="06265-196">CardPaymentAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-196">CardPaymentAuthorizePaymentRequest</span></span>                     |
| <span data-ttu-id="06265-197">CardPaymentBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="06265-197">CardPaymentBeginTransactionRequest</span></span>                     |
| <span data-ttu-id="06265-198">CardPaymentCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-198">CardPaymentCapturePaymentRequest</span></span>                       |
| <span data-ttu-id="06265-199">CardPaymentEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="06265-199">CardPaymentEndTransactionRequest</span></span>                       |
| <span data-ttu-id="06265-200">CardPaymentEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="06265-200">CardPaymentEnquireGiftCardBalancePeripheralRequest</span></span>     |
| <span data-ttu-id="06265-201">CardPaymentExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="06265-201">CardPaymentExecuteTaskRequest</span></span>                          |
| <span data-ttu-id="06265-202">CardPaymentRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-202">CardPaymentRefundPaymentRequest</span></span>                        |
| <span data-ttu-id="06265-203">CardPaymentVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-203">CardPaymentVoidPaymentRequest</span></span>                          |
| <span data-ttu-id="06265-204">CashDrawerIsOpenRequest</span><span class="sxs-lookup"><span data-stu-id="06265-204">CashDrawerIsOpenRequest</span></span>                                |
| <span data-ttu-id="06265-205">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="06265-205">HardwareStationDeviceActionRequest</span></span>                     |
| <span data-ttu-id="06265-206">HardwareStationStatusRequest</span><span class="sxs-lookup"><span data-stu-id="06265-206">HardwareStationStatusRequest</span></span>                           |
| <span data-ttu-id="06265-207">LineDisplayDisplayLinesRequest</span><span class="sxs-lookup"><span data-stu-id="06265-207">LineDisplayDisplayLinesRequest</span></span>                         |
| <span data-ttu-id="06265-208">PaymentTerminalAuthorizePaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="06265-208">PaymentTerminalAuthorizePaymentActivityRequest</span></span>         |
| <span data-ttu-id="06265-209">PaymentTerminalAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-209">PaymentTerminalAuthorizePaymentRequest</span></span>                 |
| <span data-ttu-id="06265-210">PaymentTerminalBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="06265-210">PaymentTerminalBeginTransactionRequest</span></span>                 |
| <span data-ttu-id="06265-211">PaymentTerminalCancelOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-211">PaymentTerminalCancelOperationRequest</span></span>                  |
| <span data-ttu-id="06265-212">PaymentTerminalCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-212">PaymentTerminalCapturePaymentRequest</span></span>                   |
| <span data-ttu-id="06265-213">PaymentTerminalEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="06265-213">PaymentTerminalEndTransactionRequest</span></span>                   |
| <span data-ttu-id="06265-214">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="06265-214">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span></span> |
| <span data-ttu-id="06265-215">PaymentTerminalExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="06265-215">PaymentTerminalExecuteTaskRequest</span></span>                      |
| <span data-ttu-id="06265-216">PaymentTerminalRefundPaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="06265-216">PaymentTerminalRefundPaymentActivityRequest</span></span>            |
| <span data-ttu-id="06265-217">PaymentTerminalRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-217">PaymentTerminalRefundPaymentRequest</span></span>                    |
| <span data-ttu-id="06265-218">PaymentTerminalUpdateLinesRequest</span><span class="sxs-lookup"><span data-stu-id="06265-218">PaymentTerminalUpdateLinesRequest</span></span>                      |
| <span data-ttu-id="06265-219">PaymentTerminalVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="06265-219">PaymentTerminalVoidPaymentRequest</span></span>                      |
| <span data-ttu-id="06265-220">PrinterPrintRequest</span><span class="sxs-lookup"><span data-stu-id="06265-220">PrinterPrintRequest</span></span>                                    |
| <span data-ttu-id="06265-221">ScaleReadRequest</span><span class="sxs-lookup"><span data-stu-id="06265-221">ScaleReadRequest</span></span>                                       |

### <a name="scanresults"></a><span data-ttu-id="06265-222">ScanResults</span><span class="sxs-lookup"><span data-stu-id="06265-222">ScanResults</span></span>

<span data-ttu-id="06265-223">次に、スキャン結果に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-223">The following is a list of APIs exposed to perform scan results-related functionality.</span></span>

| <span data-ttu-id="06265-224">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-224">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="06265-225">GetScanResultClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-225">GetScanResultClientRequest</span></span> |

### <a name="customer"></a><span data-ttu-id="06265-226">顧客</span><span class="sxs-lookup"><span data-stu-id="06265-226">Customer</span></span>

<span data-ttu-id="06265-227">次に、顧客に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-227">The following is a list of APIs exposed to perform customer-related functionality.</span></span>

| <span data-ttu-id="06265-228">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-228">POS API</span></span>                  |
|--------------------------|
| <span data-ttu-id="06265-229">GetCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-229">GetCustomerClientRequest</span></span> |
|<span data-ttu-id="06265-230">CreateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-230">CreateCustomerServiceRequest</span></span> |
|<span data-ttu-id="06265-231">UpdateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-231">UpdateCustomerServiceRequest</span></span> |
|<span data-ttu-id="06265-232">SelectCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-232">SelectCustomerClientRequest</span></span> |


### <a name="authentication"></a><span data-ttu-id="06265-233">認証</span><span class="sxs-lookup"><span data-stu-id="06265-233">Authentication</span></span>

<span data-ttu-id="06265-234">次に、認証に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-234">The following is a list of APIs exposed to perform authentication-related functionality.</span></span>

| <span data-ttu-id="06265-235">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-235">POS API</span></span>                |
|------------------------|
| <span data-ttu-id="06265-236">LogOffOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-236">LogOffOperationRequest</span></span> |

### <a name="dataservice"></a><span data-ttu-id="06265-237">DataService</span><span class="sxs-lookup"><span data-stu-id="06265-237">DataService</span></span>

<span data-ttu-id="06265-238">次に、データ サービスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-238">The following is a list of APIs exposed to perform data service-related functionality.</span></span>

| <span data-ttu-id="06265-239">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-239">POS API</span></span>            |
|--------------------|
| <span data-ttu-id="06265-240">DataServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-240">DataServiceRequest</span></span> |

### <a name="device"></a><span data-ttu-id="06265-241">デバイス</span><span class="sxs-lookup"><span data-stu-id="06265-241">Device</span></span>

<span data-ttu-id="06265-242">次に、デバイスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-242">The following is a list of APIs exposed to perform device-related functionality.</span></span>

| <span data-ttu-id="06265-243">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-243">POS API</span></span>                               |
|---------------------------------------|
| <span data-ttu-id="06265-244">GetDeviceConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-244">GetDeviceConfigurationClientRequest</span></span>   |
| <span data-ttu-id="06265-245">GetExtensionProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-245">GetExtensionProfileClientRequest</span></span>      |
| <span data-ttu-id="06265-246">GetHardwareProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-246">GetHardwareProfileClientRequest</span></span>       |
| <span data-ttu-id="06265-247">GetAuthenticationTokenClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-247">GetAuthenticationTokenClientRequest</span></span>   |
| <span data-ttu-id="06265-248">GetConnectionStatusClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-248">GetConnectionStatusClientRequest</span></span>      |
| <span data-ttu-id="06265-249">GetActiveHardwareStationClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-249">GetActiveHardwareStationClientRequest</span></span> |
| <span data-ttu-id="06265-250">GetApplicationVersionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-250">GetApplicationVersionClientRequest</span></span>    |
| <span data-ttu-id="06265-251">GetChannelConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-251">GetChannelConfigurationClientRequest</span></span>  |

### <a name="diagnostics"></a><span data-ttu-id="06265-252">診断</span><span class="sxs-lookup"><span data-stu-id="06265-252">Diagnostics</span></span> 

<span data-ttu-id="06265-253">次に、診断に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-253">The following is a list of APIs exposed to perform diagnostics-related functionality.</span></span>

| <span data-ttu-id="06265-254">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-254">POS API</span></span>                     |
|-----------------------------|
| <span data-ttu-id="06265-255">GetSessionInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-255">GetSessionInfoClientRequest</span></span> |

### <a name="dialog"></a><span data-ttu-id="06265-256">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="06265-256">Dialog</span></span>

<span data-ttu-id="06265-257">次に、ダイアログに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-257">The following is a list of APIs exposed to perform dialog-related functionality.</span></span>

| <span data-ttu-id="06265-258">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-258">POS API</span></span>                                  |
|------------------------------------------|
| <span data-ttu-id="06265-259">ShowMessageDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-259">ShowMessageDialogClientRequest</span></span>           |
| <span data-ttu-id="06265-260">IAlphanumericInputDialogResult</span><span class="sxs-lookup"><span data-stu-id="06265-260">IAlphanumericInputDialogResult</span></span>           |
| <span data-ttu-id="06265-261">ShowAlphanumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-261">ShowAlphanumericInputDialogClientRequest</span></span> |
| <span data-ttu-id="06265-262">ShowNumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-262">ShowNumericInputDialogClientRequest</span></span>      |
| <span data-ttu-id="06265-263">ShowListInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-263">ShowListInputDialogClientRequest</span></span>         |
| <span data-ttu-id="06265-264">ShowTextInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-264">ShowTextInputDialogClientRequest</span></span>         |

### <a name="employee"></a><span data-ttu-id="06265-265">従業員</span><span class="sxs-lookup"><span data-stu-id="06265-265">Employee</span></span>

<span data-ttu-id="06265-266">次に、従業員に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-266">The following is a list of APIs exposed to perform employee-related functionality.</span></span>

| <span data-ttu-id="06265-267">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-267">POS API</span></span>                          |
|----------------------------------|
| <span data-ttu-id="06265-268">GetLoggedOnEmployeeClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-268">GetLoggedOnEmployeeClientRequest</span></span> |

### <a name="formatters"></a><span data-ttu-id="06265-269">フォーマッター</span><span class="sxs-lookup"><span data-stu-id="06265-269">Formatters</span></span>

<span data-ttu-id="06265-270">次に、フォーマッターに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-270">The following is a list of APIs exposed to perform formatter-related functionality.</span></span>

| <span data-ttu-id="06265-271">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-271">POS API</span></span>                             |
|-------------------------------------|
| <span data-ttu-id="06265-272">IBooleanFormatter</span><span class="sxs-lookup"><span data-stu-id="06265-272">IBooleanFormatter</span></span>                   |
| <span data-ttu-id="06265-273">ICurrencyFormatter</span><span class="sxs-lookup"><span data-stu-id="06265-273">ICurrencyFormatter</span></span>                  |
| <span data-ttu-id="06265-274">IDateFormatter</span><span class="sxs-lookup"><span data-stu-id="06265-274">IDateFormatter</span></span>                      |
| <span data-ttu-id="06265-275">ITransactionTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="06265-275">ITransactionTypeFormatter</span></span>           |
| <span data-ttu-id="06265-276">IPurchaseTransferOrderTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="06265-276">IPurchaseTransferOrderTypeFormatter</span></span> |

### <a name="orgunits"></a><span data-ttu-id="06265-277">OrgUnits</span><span class="sxs-lookup"><span data-stu-id="06265-277">OrgUnits</span></span>

<span data-ttu-id="06265-278">次に、組織単位に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-278">The following is a list of APIs exposed to perform org units-related functionality.</span></span>

| <span data-ttu-id="06265-279">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-279">POS API</span></span>                              |
|--------------------------------------|
| <span data-ttu-id="06265-280">GetOrgUnitConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-280">GetOrgUnitConfigurationClientRequest</span></span> |
| <span data-ttu-id="06265-281">GetOrgUnitTenderTypesClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-281">GetOrgUnitTenderTypesClientRequest</span></span>   |
| <span data-ttu-id="06265-282">InventoryLookupOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-282">InventoryLookupOperationRequest</span></span>      |

### <a name="products"></a><span data-ttu-id="06265-283">製品</span><span class="sxs-lookup"><span data-stu-id="06265-283">Products</span></span>

<span data-ttu-id="06265-284">次に、製品に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-284">The following is a list of APIs exposed to perform products-related functionality.</span></span>

| <span data-ttu-id="06265-285">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-285">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="06265-286">GetProductsByIdsClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-286">GetProductsByIdsClientRequest</span></span>              |
| <span data-ttu-id="06265-287">GetCurrentProductCatalogStoreClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-287">GetCurrentProductCatalogStoreClientRequest</span></span> |
| <span data-ttu-id="06265-288">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-288">SelectProductVariantClientRequest</span></span>          |
| <span data-ttu-id="06265-289">GetSerialNumberClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-289">GetSerialNumberClientRequest</span></span>               |
| <span data-ttu-id="06265-290">GetRefinerValuesByTextServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-290">GetRefinerValuesByTextServiceRequest</span></span>       |
| <span data-ttu-id="06265-291">SelectProductClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-291">SelectProductClientRequest</span></span> |

### <a name="salesorders"></a><span data-ttu-id="06265-292">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="06265-292">SalesOrders</span></span>

<span data-ttu-id="06265-293">次に、販売注文に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-293">The following is a list of APIs exposed to perform sales orders-related functionality.</span></span>

| <span data-ttu-id="06265-294">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-294">POS API</span></span>                                          |
|--------------------------------------------------|
| <span data-ttu-id="06265-295">GetReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-295">GetReceiptsClientRequest</span></span>                         |
| <span data-ttu-id="06265-296">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="06265-296">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="06265-297">GetSalesOrderDetailsByTransactionIdClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-297">GetSalesOrderDetailsByTransactionIdClientRequest</span></span> |
| <span data-ttu-id="06265-298">GetGiftReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-298">GetGiftReceiptsClientRequest</span></span>                     |
| <span data-ttu-id="06265-299">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="06265-299">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="06265-300">MarkAsPickedServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-300">MarkAsPickedServiceRequest</span></span>                       |
| <span data-ttu-id="06265-301">PrintPackingSlipClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-301">PrintPackingSlipClientRequest</span></span>                    |

### <a name="shifts"></a><span data-ttu-id="06265-302">シフト</span><span class="sxs-lookup"><span data-stu-id="06265-302">Shifts</span></span>

<span data-ttu-id="06265-303">次に、シフトに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-303">The following is a list of APIs exposed to perform shifts-related functionality.</span></span>

| <span data-ttu-id="06265-304">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-304">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="06265-305">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-305">CloseShiftOperationRequest</span></span> |
| <span data-ttu-id="06265-306">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-306">CloseShiftOperationRequest</span></span> |

### <a name="stockcountjournals"></a><span data-ttu-id="06265-307">StockCountJournals</span><span class="sxs-lookup"><span data-stu-id="06265-307">StockCountJournals</span></span>

<span data-ttu-id="06265-308">次に、在庫数仕訳帳に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-308">The following is a list of APIs exposed to perform stock count journals-related functionality.</span></span>

| <span data-ttu-id="06265-309">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-309">POS API</span></span>                                |
|----------------------------------------|
| <span data-ttu-id="06265-310">SyncAllStockCountJournalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-310">SyncAllStockCountJournalsClientRequest</span></span> |

### <a name="storeoperations"></a><span data-ttu-id="06265-311">StoreOperations</span><span class="sxs-lookup"><span data-stu-id="06265-311">StoreOperations</span></span>

<span data-ttu-id="06265-312">次に、店舗運営に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="06265-312">The following is a list of APIs exposed to perform store operations-related functionality.</span></span>

| <span data-ttu-id="06265-313">POS API</span><span class="sxs-lookup"><span data-stu-id="06265-313">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="06265-314">DeclareStartingAmountClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-314">DeclareStartingAmountClientRequest</span></span>              |
| <span data-ttu-id="06265-315">GetSalesOrdersWithNoFiscalTransactionsRequest</span><span class="sxs-lookup"><span data-stu-id="06265-315">GetSalesOrdersWithNoFiscalTransactionsRequest</span></span>   |
| <span data-ttu-id="06265-316">RegisterCustomAuditEventClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-316">RegisterCustomAuditEventClientRequest</span></span>           |
| <span data-ttu-id="06265-317">GetOfflinePendingTransactionCountClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-317">GetOfflinePendingTransactionCountClientRequest</span></span>  |
| <span data-ttu-id="06265-318">SaveFiscalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-318">SaveFiscalTransactionClientRequest</span></span>              |
| <span data-ttu-id="06265-319">SafeDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-319">SafeDropOperationRequest</span></span>                        |
| <span data-ttu-id="06265-320">TenderDeclarationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-320">TenderDeclarationOperationRequest</span></span>               |
| <span data-ttu-id="06265-321">TenderRemovalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-321">TenderRemovalOperationRequest</span></span>                   |
| <span data-ttu-id="06265-322">CreateBankDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-322">CreateBankDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="06265-323">CreateFloatEntryTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-323">CreateFloatEntryTransactionClientRequest</span></span>        |
| <span data-ttu-id="06265-324">CreateStartingAmountTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-324">CreateStartingAmountTransactionClientRequest</span></span>    |
| <span data-ttu-id="06265-325">CreateTenderDeclarationTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-325">CreateTenderDeclarationTransactionClientRequest</span></span> |
| <span data-ttu-id="06265-326">CreateTenderRemovalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-326">CreateTenderRemovalTransactionClientRequest</span></span>     |
| <span data-ttu-id="06265-327">GetDenominationTotalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-327">GetDenominationTotalsClientRequest</span></span>              |
| <span data-ttu-id="06265-328">SelectZipCodeInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-328">SelectZipCodeInfoClientRequest</span></span>                  |
| <span data-ttu-id="06265-329">CreateSafeDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-329">CreateSafeDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="06265-330">GetTenderDetailsClientRequest</span><span class="sxs-lookup"><span data-stu-id="06265-330">GetTenderDetailsClientRequest</span></span>                   |
| <span data-ttu-id="06265-331">LoyaltyCardPointsBalanceOperationRequest</span><span class="sxs-lookup"><span data-stu-id="06265-331">LoyaltyCardPointsBalanceOperationRequest</span></span>        |
| <span data-ttu-id="06265-332">GetCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-332">GetCommissionSalesGroupsServiceRequest</span></span>          |
| <span data-ttu-id="06265-333">GetCurrenciesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-333">GetCurrenciesServiceRequest</span></span>                     |
| <span data-ttu-id="06265-334">GetSrsReportDataSetServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-334">GetSrsReportDataSetServiceRequest</span></span>               |
| <span data-ttu-id="06265-335">SearchCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="06265-335">SearchCommissionSalesGroupsServiceRequest</span></span>       |

