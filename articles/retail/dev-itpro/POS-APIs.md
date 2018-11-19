---
title: Retail POS API
description: "このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。"
author: mugunthanm
manager: AnnBe
ms.date: 10/29/2018
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
ms.sourcegitcommit: b7f970f681872cd938a15f9aea469df1e9e1bce3
ms.openlocfilehash: e86ca46515581fea17e4312c7ce01695dd7bb482
ms.contentlocale: ja-jp
ms.lasthandoff: 11/05/2018

---
# <a name="retail-pos-apis"></a><span data-ttu-id="3cc56-103">Retail POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-103">Retail POS APIs</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cc56-104">Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-104">Retail POS APIs help you to easily build extensions or new features to the POS app.</span></span> <span data-ttu-id="3cc56-105">たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。</span><span class="sxs-lookup"><span data-stu-id="3cc56-105">For example, if you are extending the Retail POS application to add new features in which to want to get product details, change prices, or add items to a cart.</span></span> <span data-ttu-id="3cc56-106">これを実現する API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-106">you can consume APIs that will do the work for you.</span></span> <span data-ttu-id="3cc56-107">これを行うには、作業を実行する API を呼び出す必要があるだけです。</span><span class="sxs-lookup"><span data-stu-id="3cc56-107">To do this, you need to simply call the APIs to do the work.</span></span> <span data-ttu-id="3cc56-108">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-108">The POS API simplifies the extension pattern and provides continuous support to build the extensions.</span></span>

<span data-ttu-id="3cc56-109">拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。</span><span class="sxs-lookup"><span data-stu-id="3cc56-109">Extension patterns have been unified across commerce runtime (CRT), POS, and Hardware station (HWS) by following the request/response pattern.</span></span> <span data-ttu-id="3cc56-110">すべての POS API は、CRT や HWS のような要求/応答として公開されます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-110">All the POS APIs are exposed as request/response like CRT and HWS.</span></span> <span data-ttu-id="3cc56-111">このトピックは、最新の修正プログラムが適用された Dynamics 365 for Finance and Operations または Dynamics 365 for Retail に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-111">This topic is applicable for Dynamics 365 for Finance and Operations or Dynamics 365 for Retail with the latest hotfix.</span></span> 

<span data-ttu-id="3cc56-112">POS API は、3 つのさまざまなシナリオに分類されます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-112">POS APIs are categorized into three different scenarios:</span></span>

- <span data-ttu-id="3cc56-113">**消費** - 拡張機能のパブリック API を使用します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-113">**Consume** – Consume public APIs in your extension.</span></span>

- <span data-ttu-id="3cc56-114">**拡張** - 一部の追加ロジックを実行するパブリック API をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3cc56-114">**Extend** – Override public APIs to do some additional logic.</span></span>

- <span data-ttu-id="3cc56-115">**作成** - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-115">**Create** – Create new APIs using the exposed POS interface, which can be used across extensions.</span></span>

<span data-ttu-id="3cc56-116">API の多くは、拡張機能で消費できます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-116">Many APIs can be consumed in extensions.</span></span> <span data-ttu-id="3cc56-117">たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-117">For example, if you want to change the price of the item based on an external web service call, you can call PriceOverrideOperationRequest to change the price of the item.</span></span> <span data-ttu-id="3cc56-118">消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-118">Within the consume, the APIs are sub categorized by module like cart, peripherals, store operations, etc.</span></span>

> [!NOTE]
> <span data-ttu-id="3cc56-119">すべての API の一覧は、**Pos.Api.d.ts** にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。</span><span class="sxs-lookup"><span data-stu-id="3cc56-119">A list of the all of the APIs is available in **Pos.Api.d.ts**, which is part of the Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts).</span></span>

## <a name="how-to-consume-apis-in-your-extension"></a><span data-ttu-id="3cc56-120">拡張機能で API を使用する方法</span><span class="sxs-lookup"><span data-stu-id="3cc56-120">How to consume APIs in your extension</span></span>

<span data-ttu-id="3cc56-121">拡張機能で Retail API を利用するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-121">Use the following steps to consume Retail APIs in your extensions.</span></span>

1.  <span data-ttu-id="3cc56-122">拡張機能ファイルで API をインポートします。</span><span class="sxs-lookup"><span data-stu-id="3cc56-122">Import the API in your extension file.</span></span>

    <span data-ttu-id="3cc56-123">たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cc56-123">For example, if you want to consume the save attribute on cart API in your extension, then you need to add the following import statements.</span></span>

 <span data-ttu-id="3cc56-124">パターンは、"PosApi/Consume/Module name"; からの { API 名 } のインポートです</span><span class="sxs-lookup"><span data-stu-id="3cc56-124">The pattern is import { api name } from "PosApi/Consume/Module name";</span></span>
```Typescript
 import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
```

2.  <span data-ttu-id="3cc56-125">必要な場合は、クライアントのエンティティとプロキシ エンティティをインポートします。</span><span class="sxs-lookup"><span data-stu-id="3cc56-125">Import the client entities and proxy entities if required.</span></span>

```Typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
```
3.  <span data-ttu-id="3cc56-126">API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3cc56-126">Declare the API variable and execute it using the POS runtime, which you can access the runtime by using: this.context.runtime.executeAsync("api name")</span></span>

```Typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
```

 <span data-ttu-id="3cc56-127">たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cc56-127">For example, if you want to execute the tender removal, use SaveAttributesOnCartClientRequest api, and refer to the following steps.</span></span>
```Typescript
let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();

 attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;

 attributeValue.TextValue = "Yes";

 let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];

 let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =

new SaveAttributesOnCartClientRequest(attributeValues);

result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);

```
### <a name="samples-showing-how-to-access-apis"></a><span data-ttu-id="3cc56-128">API にアクセスする方法を示すサンプル</span><span class="sxs-lookup"><span data-stu-id="3cc56-128">Samples showing how to access APIs</span></span>

<span data-ttu-id="3cc56-129">**現在の買い物カゴを取得**</span><span class="sxs-lookup"><span data-stu-id="3cc56-129">**Get Current cart**</span></span>
```
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```
<span data-ttu-id="3cc56-130">**買い物カゴに追加された現在の顧客を取得**</span><span class="sxs-lookup"><span data-stu-id="3cc56-130">**Get Current customer added to cart**</span></span>
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
<span data-ttu-id="3cc56-131">**強制無効トランザクション**</span><span class="sxs-lookup"><span data-stu-id="3cc56-131">**Force void transaction**</span></span>
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

### <a name="cart"></a><span data-ttu-id="3cc56-132">カート</span><span class="sxs-lookup"><span data-stu-id="3cc56-132">Cart</span></span>

<span data-ttu-id="3cc56-133">次に、買い物カゴに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-133">The following is a list of APIs exposed to perform cart-related functionality.</span></span>

| <span data-ttu-id="3cc56-134">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-134">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="3cc56-135">AddPreprocessedTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-135">AddPreprocessedTenderLineToCartClientRequest</span></span>    |
| <span data-ttu-id="3cc56-136">AddTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-136">AddTenderLineToCartClientRequest</span></span>                |
| <span data-ttu-id="3cc56-137">ConcludeTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-137">ConcludeTransactionClientRequest</span></span>                |
| <span data-ttu-id="3cc56-138">GetCurrentCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-138">GetCurrentCartClientRequest</span></span>                     |
| <span data-ttu-id="3cc56-139">GetCurrentCartClientResponse</span><span class="sxs-lookup"><span data-stu-id="3cc56-139">GetCurrentCartClientResponse</span></span>                    |
| <span data-ttu-id="3cc56-140">GetKeyedInPriceClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-140">GetKeyedInPriceClientRequest</span></span>                    |
| <span data-ttu-id="3cc56-141">GetPickupDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-141">GetPickupDateClientRequest</span></span>                      |
| <span data-ttu-id="3cc56-142">GetReasonCodeLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-142">GetReasonCodeLinesClientRequest</span></span>                 |
| <span data-ttu-id="3cc56-143">GetReceiptEmailAddressClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-143">GetReceiptEmailAddressClientRequest</span></span>             |
| <span data-ttu-id="3cc56-144">GetShippingDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-144">GetShippingDateClientRequest</span></span>                    |
| <span data-ttu-id="3cc56-145">RefreshCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-145">RefreshCartClientRequest</span></span>                        |
| <span data-ttu-id="3cc56-146">ResumeSuspendedCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-146">ResumeSuspendedCartClientRequest</span></span>                |
| <span data-ttu-id="3cc56-147">SaveAttributesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-147">SaveAttributesOnCartClientRequest</span></span>               |
| <span data-ttu-id="3cc56-148">SaveAttributesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-148">SaveAttributesOnCartLinesClientRequest</span></span>          |
| <span data-ttu-id="3cc56-149">SaveExtensionPropertiesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-149">SaveExtensionPropertiesOnCartClientRequest</span></span>      |
| <span data-ttu-id="3cc56-150">SaveExtensionPropertiesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-150">SaveExtensionPropertiesOnCartLinesClientRequest</span></span> |
| <span data-ttu-id="3cc56-151">SaveReasonCodeLinesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-151">SaveReasonCodeLinesOnCartClientRequest</span></span>          |
| <span data-ttu-id="3cc56-152">SaveReasonCodeLinesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-152">SaveReasonCodeLinesOnCartLinesClientRequest</span></span>     |
| <span data-ttu-id="3cc56-153">SelectSalesLinesForPickUpClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-153">SelectSalesLinesForPickUpClientRequest</span></span>          |
| <span data-ttu-id="3cc56-154">SetCartAttributesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-154">SetCartAttributesClientRequest</span></span>                  |
| <span data-ttu-id="3cc56-155">ShowChangeDueClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-155">ShowChangeDueClientRequest</span></span>                      |
| <span data-ttu-id="3cc56-156">AddAffiliationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-156">AddAffiliationOperationRequest</span></span>                  |
| <span data-ttu-id="3cc56-157">AddItemToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-157">AddItemToCartOperationRequest</span></span>                   |
| <span data-ttu-id="3cc56-158">CalculateTotalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-158">CalculateTotalOperationRequest</span></span>                  |
| <span data-ttu-id="3cc56-159">ChangeCartLineUnitOfMeasureOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-159">ChangeCartLineUnitOfMeasureOperationRequest</span></span>     |
| <span data-ttu-id="3cc56-160">CreateCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-160">CreateCustomerOrderOperationRequest</span></span>             |
| <span data-ttu-id="3cc56-161">CreateCustomerQuoteOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-161">CreateCustomerQuoteOperationRequest</span></span>             |
| <span data-ttu-id="3cc56-162">CustomerAccountDepositOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-162">CustomerAccountDepositOperationRequest</span></span>          |
| <span data-ttu-id="3cc56-163">DepositOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-163">DepositOverrideOperationRequest</span></span>                 |
| <span data-ttu-id="3cc56-164">EditCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-164">EditCustomerOrderOperationRequest</span></span>               |
| <span data-ttu-id="3cc56-165">LineDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-165">LineDiscountAmountOperationRequest</span></span>              |
| <span data-ttu-id="3cc56-166">LineDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-166">LineDiscountPercentOperationRequest</span></span>             |
| <span data-ttu-id="3cc56-167">OverrideLineTaxFromListOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-167">OverrideLineTaxFromListOperationRequest</span></span>         |
| <span data-ttu-id="3cc56-168">OverrideLineTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-168">OverrideLineTaxOperationRequest</span></span>                 |
| <span data-ttu-id="3cc56-169">OverrideTransactionTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-169">OverrideTransactionTaxOperationRequest</span></span>          |
| <span data-ttu-id="3cc56-170">PickupAllOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-170">PickupAllOperationRequest</span></span>                       |
| <span data-ttu-id="3cc56-171">PriceOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-171">PriceOverrideOperationRequest</span></span>                   |
| <span data-ttu-id="3cc56-172">SetCartLineCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-172">SetCartLineCommentOperationRequest</span></span>              |
| <span data-ttu-id="3cc56-173">SetCartLineQuantityOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-173">SetCartLineQuantityOperationRequest</span></span>             |
| <span data-ttu-id="3cc56-174">SetCustomerOnCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-174">SetCustomerOnCartOperationRequest</span></span>               |
| <span data-ttu-id="3cc56-175">SetTransactionCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-175">SetTransactionCommentOperationRequest</span></span>           |
| <span data-ttu-id="3cc56-176">SuspendCurrentCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-176">SuspendCurrentCartOperationRequest</span></span>              |
| <span data-ttu-id="3cc56-177">TotalDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-177">TotalDiscountAmountOperationRequest</span></span>             |
| <span data-ttu-id="3cc56-178">TotalDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-178">TotalDiscountPercentOperationRequest</span></span>            |
| <span data-ttu-id="3cc56-179">VoidCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-179">VoidCartLineOperationRequest</span></span>                    |
| <span data-ttu-id="3cc56-180">VoidTenderLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-180">VoidTenderLineOperationRequest</span></span>                  |
| <span data-ttu-id="3cc56-181">VoidTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-181">VoidTransactionOperationRequest</span></span>                 |
| <span data-ttu-id="3cc56-182">CreateEmptyCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-182">CreateEmptyCartServiceRequest</span></span>                   |
| <span data-ttu-id="3cc56-183">GetTaxOverridesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-183">GetTaxOverridesServiceRequest</span></span>                   |
| <span data-ttu-id="3cc56-184">UpdateTenderLineSignatureServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-184">UpdateTenderLineSignatureServiceRequest</span></span>         |

### <a name="payments"></a><span data-ttu-id="3cc56-185">支払利息</span><span class="sxs-lookup"><span data-stu-id="3cc56-185">Payments</span></span>

<span data-ttu-id="3cc56-186">次に、支払に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-186">The following is a list of APIs exposed to perform payment-related functionality.</span></span>

| <span data-ttu-id="3cc56-187">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-187">POS API</span></span>                                   |
|-------------------------------------------|
| <span data-ttu-id="3cc56-188">GetGiftCardByIdServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-188">GetGiftCardByIdServiceRequest</span></span>             |
| <span data-ttu-id="3cc56-189">GetPaymentCardTypeByBinRangeClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-189">GetPaymentCardTypeByBinRangeClientRequest</span></span> |

### <a name="peripherals"></a><span data-ttu-id="3cc56-190">周辺機器</span><span class="sxs-lookup"><span data-stu-id="3cc56-190">Peripherals</span></span>

<span data-ttu-id="3cc56-191">次に、周辺機器に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-191">The following is a list of APIs exposed to perform peripheral-related functionality.</span></span>

| <span data-ttu-id="3cc56-192">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-192">POS API</span></span>                                                |
|--------------------------------------------------------|
| <span data-ttu-id="3cc56-193">CardPaymentAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-193">CardPaymentAuthorizePaymentRequest</span></span>                     |
| <span data-ttu-id="3cc56-194">CardPaymentBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-194">CardPaymentBeginTransactionRequest</span></span>                     |
| <span data-ttu-id="3cc56-195">CardPaymentCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-195">CardPaymentCapturePaymentRequest</span></span>                       |
| <span data-ttu-id="3cc56-196">CardPaymentEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-196">CardPaymentEndTransactionRequest</span></span>                       |
| <span data-ttu-id="3cc56-197">CardPaymentEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-197">CardPaymentEnquireGiftCardBalancePeripheralRequest</span></span>     |
| <span data-ttu-id="3cc56-198">CardPaymentExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-198">CardPaymentExecuteTaskRequest</span></span>                          |
| <span data-ttu-id="3cc56-199">CardPaymentRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-199">CardPaymentRefundPaymentRequest</span></span>                        |
| <span data-ttu-id="3cc56-200">CardPaymentVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-200">CardPaymentVoidPaymentRequest</span></span>                          |
| <span data-ttu-id="3cc56-201">CashDrawerIsOpenRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-201">CashDrawerIsOpenRequest</span></span>                                |
| <span data-ttu-id="3cc56-202">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-202">HardwareStationDeviceActionRequest</span></span>                     |
| <span data-ttu-id="3cc56-203">HardwareStationStatusRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-203">HardwareStationStatusRequest</span></span>                           |
| <span data-ttu-id="3cc56-204">LineDisplayDisplayLinesRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-204">LineDisplayDisplayLinesRequest</span></span>                         |
| <span data-ttu-id="3cc56-205">PaymentTerminalAuthorizePaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-205">PaymentTerminalAuthorizePaymentActivityRequest</span></span>         |
| <span data-ttu-id="3cc56-206">PaymentTerminalAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-206">PaymentTerminalAuthorizePaymentRequest</span></span>                 |
| <span data-ttu-id="3cc56-207">PaymentTerminalBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-207">PaymentTerminalBeginTransactionRequest</span></span>                 |
| <span data-ttu-id="3cc56-208">PaymentTerminalCancelOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-208">PaymentTerminalCancelOperationRequest</span></span>                  |
| <span data-ttu-id="3cc56-209">PaymentTerminalCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-209">PaymentTerminalCapturePaymentRequest</span></span>                   |
| <span data-ttu-id="3cc56-210">PaymentTerminalEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-210">PaymentTerminalEndTransactionRequest</span></span>                   |
| <span data-ttu-id="3cc56-211">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-211">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span></span> |
| <span data-ttu-id="3cc56-212">PaymentTerminalExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-212">PaymentTerminalExecuteTaskRequest</span></span>                      |
| <span data-ttu-id="3cc56-213">PaymentTerminalRefundPaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-213">PaymentTerminalRefundPaymentActivityRequest</span></span>            |
| <span data-ttu-id="3cc56-214">PaymentTerminalRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-214">PaymentTerminalRefundPaymentRequest</span></span>                    |
| <span data-ttu-id="3cc56-215">PaymentTerminalUpdateLinesRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-215">PaymentTerminalUpdateLinesRequest</span></span>                      |
| <span data-ttu-id="3cc56-216">PaymentTerminalVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-216">PaymentTerminalVoidPaymentRequest</span></span>                      |
| <span data-ttu-id="3cc56-217">PrinterPrintRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-217">PrinterPrintRequest</span></span>                                    |
| <span data-ttu-id="3cc56-218">ScaleReadRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-218">ScaleReadRequest</span></span>                                       |

### <a name="scanresults"></a><span data-ttu-id="3cc56-219">ScanResults</span><span class="sxs-lookup"><span data-stu-id="3cc56-219">ScanResults</span></span>

<span data-ttu-id="3cc56-220">次に、スキャン結果に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-220">The following is a list of APIs exposed to perform scan results-related functionality.</span></span>

| <span data-ttu-id="3cc56-221">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-221">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="3cc56-222">GetScanResultClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-222">GetScanResultClientRequest</span></span> |

### <a name="customer"></a><span data-ttu-id="3cc56-223">顧客</span><span class="sxs-lookup"><span data-stu-id="3cc56-223">Customer</span></span>

<span data-ttu-id="3cc56-224">次に、顧客に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-224">The following is a list of APIs exposed to perform customer-related functionality.</span></span>

| <span data-ttu-id="3cc56-225">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-225">POS API</span></span>                  |
|--------------------------|
| <span data-ttu-id="3cc56-226">GetCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-226">GetCustomerClientRequest</span></span> |
|<span data-ttu-id="3cc56-227">CreateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-227">CreateCustomerServiceRequest</span></span> |
|<span data-ttu-id="3cc56-228">UpdateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-228">UpdateCustomerServiceRequest</span></span> |


### <a name="authentication"></a><span data-ttu-id="3cc56-229">認証</span><span class="sxs-lookup"><span data-stu-id="3cc56-229">Authentication</span></span>

<span data-ttu-id="3cc56-230">次に、認証に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-230">The following is a list of APIs exposed to perform authentication-related functionality.</span></span>

| <span data-ttu-id="3cc56-231">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-231">POS API</span></span>                |
|------------------------|
| <span data-ttu-id="3cc56-232">LogOffOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-232">LogOffOperationRequest</span></span> |

### <a name="dataservice"></a><span data-ttu-id="3cc56-233">DataService</span><span class="sxs-lookup"><span data-stu-id="3cc56-233">DataService</span></span>

<span data-ttu-id="3cc56-234">次に、データ サービスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-234">The following is a list of APIs exposed to perform data service-related functionality.</span></span>

| <span data-ttu-id="3cc56-235">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-235">POS API</span></span>            |
|--------------------|
| <span data-ttu-id="3cc56-236">DataServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-236">DataServiceRequest</span></span> |

### <a name="device"></a><span data-ttu-id="3cc56-237">デバイス</span><span class="sxs-lookup"><span data-stu-id="3cc56-237">Device</span></span>

<span data-ttu-id="3cc56-238">次に、デバイスに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-238">The following is a list of APIs exposed to perform device-related functionality.</span></span>

| <span data-ttu-id="3cc56-239">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-239">POS API</span></span>                               |
|---------------------------------------|
| <span data-ttu-id="3cc56-240">GetDeviceConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-240">GetDeviceConfigurationClientRequest</span></span>   |
| <span data-ttu-id="3cc56-241">GetExtensionProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-241">GetExtensionProfileClientRequest</span></span>      |
| <span data-ttu-id="3cc56-242">GetHardwareProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-242">GetHardwareProfileClientRequest</span></span>       |
| <span data-ttu-id="3cc56-243">GetAuthenticationTokenClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-243">GetAuthenticationTokenClientRequest</span></span>   |
| <span data-ttu-id="3cc56-244">GetConnectionStatusClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-244">GetConnectionStatusClientRequest</span></span>      |
| <span data-ttu-id="3cc56-245">GetActiveHardwareStationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-245">GetActiveHardwareStationClientRequest</span></span> |
| <span data-ttu-id="3cc56-246">GetApplicationVersionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-246">GetApplicationVersionClientRequest</span></span>    |
| <span data-ttu-id="3cc56-247">GetChannelConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-247">GetChannelConfigurationClientRequest</span></span>  |

### <a name="diagnostics"></a><span data-ttu-id="3cc56-248">診断</span><span class="sxs-lookup"><span data-stu-id="3cc56-248">Diagnostics</span></span> 

<span data-ttu-id="3cc56-249">次に、診断に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-249">The following is a list of APIs exposed to perform diagnostics-related functionality.</span></span>

| <span data-ttu-id="3cc56-250">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-250">POS API</span></span>                     |
|-----------------------------|
| <span data-ttu-id="3cc56-251">GetSessionInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-251">GetSessionInfoClientRequest</span></span> |

### <a name="dialog"></a><span data-ttu-id="3cc56-252">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="3cc56-252">Dialog</span></span>

<span data-ttu-id="3cc56-253">次に、ダイアログに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-253">The following is a list of APIs exposed to perform dialog-related functionality.</span></span>

| <span data-ttu-id="3cc56-254">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-254">POS API</span></span>                                  |
|------------------------------------------|
| <span data-ttu-id="3cc56-255">ShowMessageDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-255">ShowMessageDialogClientRequest</span></span>           |
| <span data-ttu-id="3cc56-256">IAlphanumericInputDialogResult</span><span class="sxs-lookup"><span data-stu-id="3cc56-256">IAlphanumericInputDialogResult</span></span>           |
| <span data-ttu-id="3cc56-257">ShowAlphanumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-257">ShowAlphanumericInputDialogClientRequest</span></span> |
| <span data-ttu-id="3cc56-258">ShowNumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-258">ShowNumericInputDialogClientRequest</span></span>      |
| <span data-ttu-id="3cc56-259">ShowListInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-259">ShowListInputDialogClientRequest</span></span>         |
| <span data-ttu-id="3cc56-260">ShowTextInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-260">ShowTextInputDialogClientRequest</span></span>         |

### <a name="employee"></a><span data-ttu-id="3cc56-261">従業員</span><span class="sxs-lookup"><span data-stu-id="3cc56-261">Employee</span></span>

<span data-ttu-id="3cc56-262">次に、従業員に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-262">The following is a list of APIs exposed to perform employee-related functionality.</span></span>

| <span data-ttu-id="3cc56-263">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-263">POS API</span></span>                          |
|----------------------------------|
| <span data-ttu-id="3cc56-264">GetLoggedOnEmployeeClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-264">GetLoggedOnEmployeeClientRequest</span></span> |

### <a name="formatters"></a><span data-ttu-id="3cc56-265">フォーマッター</span><span class="sxs-lookup"><span data-stu-id="3cc56-265">Formatters</span></span>

<span data-ttu-id="3cc56-266">次に、フォーマッターに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-266">The following is a list of APIs exposed to perform formatter-related functionality.</span></span>

| <span data-ttu-id="3cc56-267">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-267">POS API</span></span>                             |
|-------------------------------------|
| <span data-ttu-id="3cc56-268">IBooleanFormatter</span><span class="sxs-lookup"><span data-stu-id="3cc56-268">IBooleanFormatter</span></span>                   |
| <span data-ttu-id="3cc56-269">ICurrencyFormatter</span><span class="sxs-lookup"><span data-stu-id="3cc56-269">ICurrencyFormatter</span></span>                  |
| <span data-ttu-id="3cc56-270">IDateFormatter</span><span class="sxs-lookup"><span data-stu-id="3cc56-270">IDateFormatter</span></span>                      |
| <span data-ttu-id="3cc56-271">ITransactionTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="3cc56-271">ITransactionTypeFormatter</span></span>           |
| <span data-ttu-id="3cc56-272">IPurchaseTransferOrderTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="3cc56-272">IPurchaseTransferOrderTypeFormatter</span></span> |

### <a name="orgunits"></a><span data-ttu-id="3cc56-273">OrgUnits</span><span class="sxs-lookup"><span data-stu-id="3cc56-273">OrgUnits</span></span>

<span data-ttu-id="3cc56-274">次に、組織単位に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-274">The following is a list of APIs exposed to perform org units-related functionality.</span></span>

| <span data-ttu-id="3cc56-275">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-275">POS API</span></span>                              |
|--------------------------------------|
| <span data-ttu-id="3cc56-276">GetOrgUnitConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-276">GetOrgUnitConfigurationClientRequest</span></span> |
| <span data-ttu-id="3cc56-277">GetOrgUnitTenderTypesClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-277">GetOrgUnitTenderTypesClientRequest</span></span>   |
| <span data-ttu-id="3cc56-278">InventoryLookupOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-278">InventoryLookupOperationRequest</span></span>      |

### <a name="products"></a><span data-ttu-id="3cc56-279">製品</span><span class="sxs-lookup"><span data-stu-id="3cc56-279">Products</span></span>

<span data-ttu-id="3cc56-280">次に、製品に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-280">The following is a list of APIs exposed to perform products-related functionality.</span></span>

| <span data-ttu-id="3cc56-281">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-281">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="3cc56-282">GetProductsByIdsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-282">GetProductsByIdsClientRequest</span></span>              |
| <span data-ttu-id="3cc56-283">GetCurrentProductCatalogStoreClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-283">GetCurrentProductCatalogStoreClientRequest</span></span> |
| <span data-ttu-id="3cc56-284">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-284">SelectProductVariantClientRequest</span></span>          |
| <span data-ttu-id="3cc56-285">GetSerialNumberClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-285">GetSerialNumberClientRequest</span></span>               |
| <span data-ttu-id="3cc56-286">GetRefinerValuesByTextServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-286">GetRefinerValuesByTextServiceRequest</span></span>       |

### <a name="salesorders"></a><span data-ttu-id="3cc56-287">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="3cc56-287">SalesOrders</span></span>

<span data-ttu-id="3cc56-288">次に、販売注文に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-288">The following is a list of APIs exposed to perform sales orders-related functionality.</span></span>

| <span data-ttu-id="3cc56-289">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-289">POS API</span></span>                                          |
|--------------------------------------------------|
| <span data-ttu-id="3cc56-290">GetReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-290">GetReceiptsClientRequest</span></span>                         |
| <span data-ttu-id="3cc56-291">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-291">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="3cc56-292">GetSalesOrderDetailsByTransactionIdClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-292">GetSalesOrderDetailsByTransactionIdClientRequest</span></span> |
| <span data-ttu-id="3cc56-293">GetGiftReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-293">GetGiftReceiptsClientRequest</span></span>                     |
| <span data-ttu-id="3cc56-294">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-294">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="3cc56-295">MarkAsPickedServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-295">MarkAsPickedServiceRequest</span></span>                       |
| <span data-ttu-id="3cc56-296">PrintPackingSlipClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-296">PrintPackingSlipClientRequest</span></span>                    |

### <a name="shifts"></a><span data-ttu-id="3cc56-297">シフト</span><span class="sxs-lookup"><span data-stu-id="3cc56-297">Shifts</span></span>

<span data-ttu-id="3cc56-298">次に、シフトに関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-298">The following is a list of APIs exposed to perform shifts-related functionality.</span></span>

| <span data-ttu-id="3cc56-299">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-299">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="3cc56-300">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-300">CloseShiftOperationRequest</span></span> |
| <span data-ttu-id="3cc56-301">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-301">CloseShiftOperationRequest</span></span> |

### <a name="stockcountjournals"></a><span data-ttu-id="3cc56-302">StockCountJournals</span><span class="sxs-lookup"><span data-stu-id="3cc56-302">StockCountJournals</span></span>

<span data-ttu-id="3cc56-303">次に、在庫数仕訳帳に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-303">The following is a list of APIs exposed to perform stock count journals-related functionality.</span></span>

| <span data-ttu-id="3cc56-304">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-304">POS API</span></span>                                |
|----------------------------------------|
| <span data-ttu-id="3cc56-305">SyncAllStockCountJournalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-305">SyncAllStockCountJournalsClientRequest</span></span> |

### <a name="storeoperations"></a><span data-ttu-id="3cc56-306">StoreOperations</span><span class="sxs-lookup"><span data-stu-id="3cc56-306">StoreOperations</span></span>

<span data-ttu-id="3cc56-307">次に、店舗運営に関連する機能を実行する公開されている API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc56-307">The following is a list of APIs exposed to perform store operations-related functionality.</span></span>

| <span data-ttu-id="3cc56-308">POS API</span><span class="sxs-lookup"><span data-stu-id="3cc56-308">POS API</span></span>                                         |
|-------------------------------------------------|
| <span data-ttu-id="3cc56-309">DeclareStartingAmountClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-309">DeclareStartingAmountClientRequest</span></span>              |
| <span data-ttu-id="3cc56-310">GetSalesOrdersWithNoFiscalTransactionsRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-310">GetSalesOrdersWithNoFiscalTransactionsRequest</span></span>   |
| <span data-ttu-id="3cc56-311">RegisterCustomAuditEventClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-311">RegisterCustomAuditEventClientRequest</span></span>           |
| <span data-ttu-id="3cc56-312">GetOfflinePendingTransactionCountClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-312">GetOfflinePendingTransactionCountClientRequest</span></span>  |
| <span data-ttu-id="3cc56-313">SaveFiscalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-313">SaveFiscalTransactionClientRequest</span></span>              |
| <span data-ttu-id="3cc56-314">SafeDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-314">SafeDropOperationRequest</span></span>                        |
| <span data-ttu-id="3cc56-315">TenderDeclarationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-315">TenderDeclarationOperationRequest</span></span>               |
| <span data-ttu-id="3cc56-316">TenderRemovalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-316">TenderRemovalOperationRequest</span></span>                   |
| <span data-ttu-id="3cc56-317">CreateBankDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-317">CreateBankDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="3cc56-318">CreateFloatEntryTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-318">CreateFloatEntryTransactionClientRequest</span></span>        |
| <span data-ttu-id="3cc56-319">CreateStartingAmountTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-319">CreateStartingAmountTransactionClientRequest</span></span>    |
| <span data-ttu-id="3cc56-320">CreateTenderDeclarationTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-320">CreateTenderDeclarationTransactionClientRequest</span></span> |
| <span data-ttu-id="3cc56-321">CreateTenderRemovalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-321">CreateTenderRemovalTransactionClientRequest</span></span>     |
| <span data-ttu-id="3cc56-322">GetDenominationTotalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-322">GetDenominationTotalsClientRequest</span></span>              |
| <span data-ttu-id="3cc56-323">SelectZipCodeInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-323">SelectZipCodeInfoClientRequest</span></span>                  |
| <span data-ttu-id="3cc56-324">CreateSafeDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-324">CreateSafeDropTransactionClientRequest</span></span>          |
| <span data-ttu-id="3cc56-325">GetTenderDetailsClientRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-325">GetTenderDetailsClientRequest</span></span>                   |
| <span data-ttu-id="3cc56-326">LoyaltyCardPointsBalanceOperationRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-326">LoyaltyCardPointsBalanceOperationRequest</span></span>        |
| <span data-ttu-id="3cc56-327">GetCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-327">GetCommissionSalesGroupsServiceRequest</span></span>          |
| <span data-ttu-id="3cc56-328">GetCurrenciesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-328">GetCurrenciesServiceRequest</span></span>                     |
| <span data-ttu-id="3cc56-329">GetSrsReportDataSetServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-329">GetSrsReportDataSetServiceRequest</span></span>               |
| <span data-ttu-id="3cc56-330">SearchCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="3cc56-330">SearchCommissionSalesGroupsServiceRequest</span></span>       |

