---
title: 販売時点管理 (POS) API
description: このトピックでは、使用可能な POS API の一覧とそれらにアクセスする方法を示します。
author: mugunthanm
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-10-29
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: 7c81efba2c1a03e18dc0c43b5a44ee69303ff147
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793041"
---
# <a name="point-of-sale-pos-apis"></a><span data-ttu-id="c21c3-103">販売時点管理 (POS) API</span><span class="sxs-lookup"><span data-stu-id="c21c3-103">Point of sale (POS) APIs</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c21c3-104">Retail POS API を使用すると、簡単に POS アプリに拡張機能または新しい機能を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-104">Retail POS APIs help you to easily build extensions or new features to the POS app.</span></span> <span data-ttu-id="c21c3-105">たとえば、製品の詳細の取得、価格の変更、買い物カゴへの品目の追加を行うための新しい機能を追加するために Retail POS アプリケーションを拡張する場合です。</span><span class="sxs-lookup"><span data-stu-id="c21c3-105">For example, if you are extending the Retail POS application to add new features in which to want to get product details, change prices, or add items to a cart.</span></span> <span data-ttu-id="c21c3-106">これを実現する API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-106">you can consume APIs that will do the work for you.</span></span> <span data-ttu-id="c21c3-107">これを行うには、作業を実行する API を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c21c3-107">To do this, you need to call the APIs to do the work.</span></span> <span data-ttu-id="c21c3-108">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-108">The POS API simplifies the extension pattern and provides continuous support to build the extensions.</span></span>

<span data-ttu-id="c21c3-109">拡張パターンは、要求/応答のパターンに従って Commerce Runtime (CRT)、POS、ハードウェア ステーション (HWS) 間で統合されています。</span><span class="sxs-lookup"><span data-stu-id="c21c3-109">Extension patterns have been unified across commerce runtime (CRT), POS, and Hardware station (HWS) by following the request/response pattern.</span></span> <span data-ttu-id="c21c3-110">すべての POS API は、CRT や HWS のような要求/応答として公開されます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-110">All the POS APIs are exposed as request/response like CRT and HWS.</span></span> 

<span data-ttu-id="c21c3-111">POS API は、3 つのさまざまなシナリオに分類されます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-111">POS APIs are categorized into three different scenarios:</span></span>

- <span data-ttu-id="c21c3-112">**消費** - 拡張機能のパブリック API を使用します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-112">**Consume** – Consume public APIs in your extension.</span></span>

- <span data-ttu-id="c21c3-113">**拡張** - 一部の追加ロジックを実行するパブリック API をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-113">**Extend** – Override public APIs to do some additional logic.</span></span>

- <span data-ttu-id="c21c3-114">**作成** - 公開された POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-114">**Create** – Create new APIs using the exposed POS interface, which can be used across extensions.</span></span>

<span data-ttu-id="c21c3-115">API の多くは、拡張機能で消費できます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-115">Many APIs can be consumed in extensions.</span></span> <span data-ttu-id="c21c3-116">たとえば、外部の Web サービス コールに基づいて品目の価格を変更する場合は、品目の価格を変更する PriceOverrideOperationRequest を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-116">For example, if you want to change the price of the item based on an external web service call, you can call PriceOverrideOperationRequest to change the price of the item.</span></span> <span data-ttu-id="c21c3-117">消費では、API は買い物カゴ、周辺機器、店舗運営のようなモジュールごとにサブカテゴリに入れられます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-117">Within the consume, the APIs are sub categorized by module like cart, peripherals, store operations, etc.</span></span>

> [!NOTE]
> <span data-ttu-id="c21c3-118">すべての API の一覧は、**Pos.Api.d.ts** にあります。これは、Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts) の一部です。</span><span class="sxs-lookup"><span data-stu-id="c21c3-118">A list of the all of the APIs is available in **Pos.Api.d.ts**, which is part of the Retail SDK (...Retail SDK\POS\Extensions\Pos.Api.d.ts).</span></span> <span data-ttu-id="c21c3-119">拡張機能は、公開されている要求と、POS.Api.d.ts からの応答のみを使用する必要があり、Pos.Api.d.ts を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="c21c3-119">Extensions must consume only the exposed request and response from the POS.Api.d.ts and no modification is allowed to Pos.Api.d.ts.</span></span> <span data-ttu-id="c21c3-120">拡張機能は、POS API、プロパティ、メソッド、またはハンドラーを、POS Commerce またはセッション オブジェクトから直接使用したり更新したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c21c3-120">Extensions should not consume or update any POS APIs, properties, methods, or handlers directly from POS commerce or sessions objects.</span></span> 

## <a name="how-to-consume-apis-in-your-extension"></a><span data-ttu-id="c21c3-121">拡張機能で API を使用する方法</span><span class="sxs-lookup"><span data-stu-id="c21c3-121">How to consume APIs in your extension</span></span>

<span data-ttu-id="c21c3-122">拡張機能で Retail API を利用するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-122">Use the following steps to consume Retail APIs in your extensions.</span></span>

1.  <span data-ttu-id="c21c3-123">拡張機能ファイルで API をインポートします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-123">Import the API in your extension file.</span></span>

    <span data-ttu-id="c21c3-124">たとえば、拡張機能の買い物カゴ API で保存属性を使用する場合、次のインポート ステートメントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c21c3-124">For example, if you want to consume the save attribute on cart API in your extension, then you need to add the following import statements.</span></span>

    <span data-ttu-id="c21c3-125">パターンは、"PosApi/Consume/Module name" からの {api name} のインポートです。</span><span class="sxs-lookup"><span data-stu-id="c21c3-125">The pattern is import { api name } from "PosApi/Consume/Module name";</span></span>
 
    ```typescript
    import { SaveAttributesOnCartClientRequest, SaveAttributesOnCartClientResponse } from "PosApi/Consume/Cart";
    ```

2.  <span data-ttu-id="c21c3-126">必要に応じて、クライアントのエンティティとプロキシ エンティティをインポートします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-126">Import the client entities and proxy entities if necessary.</span></span>

    ```typescript
    import { ClientEntities } from "PosApi/Entities";

    import { ProxyEntities } from "PosApi/Entities";
    ```
3.  <span data-ttu-id="c21c3-127">API 変数を宣言し、POS ランタイムを使用して実行します。これには、this.context.runtime.executeAsync("api name") を使用してランタイムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c21c3-127">Declare the API variable and execute it using the POS runtime, which you can access the runtime by using: this.context.runtime.executeAsync("api name")</span></span>

    ```typescript
    executeAsync<TResponse extends Response>(request: Request<TResponse>): Promise<Client.Entities.ICancelableDataResult<TResponse>>;
    ```
    
    <span data-ttu-id="c21c3-128">たとえば、支払/入金の削除を実行する場合は、SaveAttributesOnCartClientRequest api を使用し、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c21c3-128">For example, if you want to execute the tender removal, use SaveAttributesOnCartClientRequest api, and refer to the following steps.</span></span>
 
    ```typescript
    let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();

     attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;

     attributeValue.TextValue = "Yes";

     let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];

     let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =

    new SaveAttributesOnCartClientRequest(attributeValues);

    result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
    ```

### <a name="samples-showing-how-to-access-apis"></a><span data-ttu-id="c21c3-129">API にアクセスする方法を示すサンプル</span><span class="sxs-lookup"><span data-stu-id="c21c3-129">Samples showing how to access APIs</span></span>

<span data-ttu-id="c21c3-130">**現在の買い物カゴを取得**</span><span class="sxs-lookup"><span data-stu-id="c21c3-130">**Get Current cart**</span></span>
```typescript
// Gets the current cart.

 let currentCart: ProxyEntities.Cart;

 return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())

 .then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):

 Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {

currentCart = getCurrentCartClientResponse.data.result;

```

<span data-ttu-id="c21c3-131">**買い物カゴに追加された現在の顧客を取得**</span><span class="sxs-lookup"><span data-stu-id="c21c3-131">**Get Current customer added to cart**</span></span>
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

<span data-ttu-id="c21c3-132">**強制無効トランザクション**</span><span class="sxs-lookup"><span data-stu-id="c21c3-132">**Force void transaction**</span></span>
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

### <a name="cart"></a><span data-ttu-id="c21c3-133">カート</span><span class="sxs-lookup"><span data-stu-id="c21c3-133">Cart</span></span>

<span data-ttu-id="c21c3-134">次の表に、買い物カゴに関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-134">The following table lists APIs exposed to perform cart-related functionality.</span></span>

| <span data-ttu-id="c21c3-135">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-135">POS API</span></span>                                   | <span data-ttu-id="c21c3-136">説明</span><span class="sxs-lookup"><span data-stu-id="c21c3-136">Description</span></span>                            | <span data-ttu-id="c21c3-137">リリース</span><span class="sxs-lookup"><span data-stu-id="c21c3-137">Release</span></span>                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| <span data-ttu-id="c21c3-138">AddPreprocessedTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-138">AddPreprocessedTenderLineToCartClientRequest</span></span>    | <span data-ttu-id="c21c3-139">事前処理済の入金明細行を買い物カゴに追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-139">Adds the pre-processed tender line to the cart.</span></span>   | <span data-ttu-id="c21c3-140">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-140">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-141">AddTenderLineToCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-141">AddTenderLineToCartClientRequest</span></span>                | <span data-ttu-id="c21c3-142">入金明細行を買い物カゴに追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-142">Adds the tender line to the cart.</span></span>  | <span data-ttu-id="c21c3-143">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-143">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-144">ConcludeTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-144">ConcludeTransactionClientRequest</span></span>                | <span data-ttu-id="c21c3-145">トランザクションを終了します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-145">Concludes the transaction.</span></span>    | <span data-ttu-id="c21c3-146">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-146">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-147">GetCurrentCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-147">GetCurrentCartClientRequest</span></span>                     | <span data-ttu-id="c21c3-148">現在の買い物カゴを取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-148">Gets the current cart.</span></span>   | <span data-ttu-id="c21c3-149">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-149">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-150">GetKeyedInPriceClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-150">GetKeyedInPriceClientRequest</span></span>                    |  <span data-ttu-id="c21c3-151">キー入力価格を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-151">Gets the keyed in price.</span></span>                                      | <span data-ttu-id="c21c3-152">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-152">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-153">GetPickupDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-153">GetPickupDateClientRequest</span></span>                      |  <span data-ttu-id="c21c3-154">集荷日を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-154">Gets the pickup date.</span></span>                                      | <span data-ttu-id="c21c3-155">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-155">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-156">GetReasonCodeLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-156">GetReasonCodeLinesClientRequest</span></span>                 |  <span data-ttu-id="c21c3-157">理由コードを取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-157">Gets the reason code.</span></span>                                      | <span data-ttu-id="c21c3-158">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-158">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-159">GetReceiptEmailAddressClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-159">GetReceiptEmailAddressClientRequest</span></span>             |  <span data-ttu-id="c21c3-160">受信電子メール アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-160">Gets the receipt email address.</span></span>                                     | <span data-ttu-id="c21c3-161">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-161">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-162">GetShippingDateClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-162">GetShippingDateClientRequest</span></span>                    |  <span data-ttu-id="c21c3-163">出荷日を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-163">Gets the shipping date.</span></span>                                      | <span data-ttu-id="c21c3-164">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-164">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-165">RefreshCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-165">RefreshCartClientRequest</span></span>                        |  <span data-ttu-id="c21c3-166">サーバーの買い物カゴ データを使用して、現在の買い物カゴを更新します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-166">Refresh the current cart with the cart data from the server.</span></span>                                      | <span data-ttu-id="c21c3-167">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-167">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-168">ResumeSuspendedCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-168">ResumeSuspendedCartClientRequest</span></span>                | <span data-ttu-id="c21c3-169">渡された ID に基づいて中断されたトランザクションを再開します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-169">Resumes the suspended transaction based on the ID passed.</span></span>                                       | <span data-ttu-id="c21c3-170">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-170">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-171">SaveAttributesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-171">SaveAttributesOnCartClientRequest</span></span>               | <span data-ttu-id="c21c3-172">買い物カゴの属性を保存します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-172">Saves the attributes on the cart.</span></span>                                       | <span data-ttu-id="c21c3-173">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-173">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-174">SaveAttributesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-174">SaveAttributesOnCartLinesClientRequest</span></span>          | <span data-ttu-id="c21c3-175">買い物カゴ内の明細行の属性を保存します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-175">Saves the attributes on the cart line.</span></span>                                       | <span data-ttu-id="c21c3-176">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-176">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-177">SaveExtensionPropertiesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-177">SaveExtensionPropertiesOnCartClientRequest</span></span>      | <span data-ttu-id="c21c3-178">買い物カゴの拡張機能プロパティを保存します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-178">Saves the extension properties on the cart.</span></span>                                        | <span data-ttu-id="c21c3-179">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-179">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-180">SaveExtensionPropertiesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-180">SaveExtensionPropertiesOnCartLinesClientRequest</span></span> | <span data-ttu-id="c21c3-181">買い物カゴ内の明細行の拡張機能プロパティを保存します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-181">Saves the extension properties on the cart line.</span></span>                                       | <span data-ttu-id="c21c3-182">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-182">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-183">SaveReasonCodeLinesOnCartClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-183">SaveReasonCodeLinesOnCartClientRequest</span></span>          | <span data-ttu-id="c21c3-184">買い物カゴに理由コードの明細行を保存します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-184">Saves the reason code lines on the cart.</span></span>                                       | <span data-ttu-id="c21c3-185">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-185">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-186">SaveReasonCodeLinesOnCartLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-186">SaveReasonCodeLinesOnCartLinesClientRequest</span></span>     |  <span data-ttu-id="c21c3-187">買い物カゴの明細行に理由コードの明細行を保存します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-187">Saves the reason code lines on the cart line.</span></span>                                      | <span data-ttu-id="c21c3-188">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-188">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-189">SelectSalesLinesForPickUpClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-189">SelectSalesLinesForPickUpClientRequest</span></span>          |  <span data-ttu-id="c21c3-190">出荷の販売明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-190">Select the sales lines for pickup.</span></span>                                      | <span data-ttu-id="c21c3-191">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-191">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-192">SetCartAttributesClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-192">SetCartAttributesClientRequest</span></span>                  |   <span data-ttu-id="c21c3-193">買い物カゴの属性を設定します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-193">Sets the cart attribute.</span></span>                                     | <span data-ttu-id="c21c3-194">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-194">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-195">ShowChangeDueClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-195">ShowChangeDueClientRequest</span></span>                      |  <span data-ttu-id="c21c3-196">期日の変更ダイアログを表示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-196">Shows the change due dialog.</span></span>                                      | <span data-ttu-id="c21c3-197">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-197">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-198">AddAffiliationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-198">AddAffiliationOperationRequest</span></span>                  |  <span data-ttu-id="c21c3-199">買い物カゴへ所属を追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-199">Adds affiliation to the cart.</span></span>                                      | <span data-ttu-id="c21c3-200">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-200">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-201">AddItemToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-201">AddItemToCartOperationRequest</span></span>                   |  <span data-ttu-id="c21c3-202">買い物カゴへ品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-202">Add items to the cart.</span></span>                                      | <span data-ttu-id="c21c3-203">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-203">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-204">CalculateTotalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-204">CalculateTotalOperationRequest</span></span>                  |  <span data-ttu-id="c21c3-205">買い物カゴの合計を計算します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-205">Calculate the total for the cart.</span></span>                                      | <span data-ttu-id="c21c3-206">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-206">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-207">ChangeCartLineUnitOfMeasureOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-207">ChangeCartLineUnitOfMeasureOperationRequest</span></span>     |  <span data-ttu-id="c21c3-208">買い物カゴ明細行の測定単位を変更します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-208">Changes the cart line unit of measure.</span></span>                                      | <span data-ttu-id="c21c3-209">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-209">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-210">CreateCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-210">CreateCustomerOrderOperationRequest</span></span>             |   <span data-ttu-id="c21c3-211">顧客注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-211">Creates the customer order.</span></span>                                     | <span data-ttu-id="c21c3-212">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-212">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-213">CreateCustomerQuoteOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-213">CreateCustomerQuoteOperationRequest</span></span>             |   <span data-ttu-id="c21c3-214">顧客見積を作成します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-214">Creates the customer quote.</span></span>                                     | <span data-ttu-id="c21c3-215">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-215">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-216">CustomerAccountDepositOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-216">CustomerAccountDepositOperationRequest</span></span>          |                                        | <span data-ttu-id="c21c3-217">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-217">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-218">DepositOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-218">DepositOverrideOperationRequest</span></span>                 |  <span data-ttu-id="c21c3-219">預金額を上書きします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-219">Overrides the deposit amount.</span></span>                                      | <span data-ttu-id="c21c3-220">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-220">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-221">EditCustomerOrderOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-221">EditCustomerOrderOperationRequest</span></span>               |   <span data-ttu-id="c21c3-222">顧客注文を編集します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-222">Edit the customer order.</span></span>                                     | <span data-ttu-id="c21c3-223">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-223">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-224">LineDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-224">LineDiscountAmountOperationRequest</span></span>              |  <span data-ttu-id="c21c3-225">明細行割引金額を買い物カゴ明細行に追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-225">Add line discount amount to the cart line.</span></span>                                      | <span data-ttu-id="c21c3-226">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-226">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-227">LineDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-227">LineDiscountPercentOperationRequest</span></span>             |  <span data-ttu-id="c21c3-228">明細行割引率を買い物カゴ明細行に追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-228">Add line discount percent to the cart line.</span></span>                                      | <span data-ttu-id="c21c3-229">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-229">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-230">OverrideLineTaxFromListOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-230">OverrideLineTaxFromListOperationRequest</span></span>         |  <span data-ttu-id="c21c3-231">一覧から買い物カゴ明細行の税を上書きします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-231">Override the cart line tax from the list.</span></span>                                      | <span data-ttu-id="c21c3-232">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-232">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-233">OverrideLineTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-233">OverrideLineTaxOperationRequest</span></span>                 |   <span data-ttu-id="c21c3-234">買い物カゴ明細行の税を上書きします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-234">Override the cart line tax.</span></span>                                     | <span data-ttu-id="c21c3-235">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-235">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-236">OverrideTransactionTaxOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-236">OverrideTransactionTaxOperationRequest</span></span>          |    <span data-ttu-id="c21c3-237">取引税を上書きします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-237">Override the transaction tax.</span></span>                                       | <span data-ttu-id="c21c3-238">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-238">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-239">PickupAllOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-239">PickupAllOperationRequest</span></span>                       |   <span data-ttu-id="c21c3-240">注文をピックアップします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-240">Picks up the order.</span></span>                                     | <span data-ttu-id="c21c3-241">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-241">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-242">PriceOverrideOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-242">PriceOverrideOperationRequest</span></span>                   | <span data-ttu-id="c21c3-243">買い物カゴ明細行の価格を上書きします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-243">Override the price for the cart line.</span></span>                                       | <span data-ttu-id="c21c3-244">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-244">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-245">SetCartLineCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-245">SetCartLineCommentOperationRequest</span></span>              |  <span data-ttu-id="c21c3-246">買い物カゴ明細行のコメントを設定します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-246">Sets the cart line comment.</span></span>                                      | <span data-ttu-id="c21c3-247">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-247">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-248">SetCartLineQuantityOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-248">SetCartLineQuantityOperationRequest</span></span>             |   <span data-ttu-id="c21c3-249">買い物カゴ明細行の数量を設定します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-249">Sets the cart line quantity.</span></span>                                     | <span data-ttu-id="c21c3-250">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-250">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-251">SetCustomerOnCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-251">SetCustomerOnCartOperationRequest</span></span>               |   <span data-ttu-id="c21c3-252">買い物カゴの顧客を設定します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-252">Sets the customer on the cart.</span></span>                                     | <span data-ttu-id="c21c3-253">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-253">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-254">SetTransactionCommentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-254">SetTransactionCommentOperationRequest</span></span>           |   <span data-ttu-id="c21c3-255">トランザクションのコメントを設定します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-255">Sets the transaction comment.</span></span>                                     | <span data-ttu-id="c21c3-256">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-256">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-257">SuspendCurrentCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-257">SuspendCurrentCartOperationRequest</span></span>              | <span data-ttu-id="c21c3-258">現在のトランザクションを中断します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-258">Suspends the current transaction.</span></span>                                       | <span data-ttu-id="c21c3-259">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-259">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-260">TotalDiscountAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-260">TotalDiscountAmountOperationRequest</span></span>             |   <span data-ttu-id="c21c3-261">トランザクションへ合計割引金額を追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-261">Add total discount amount to the transaction.</span></span>                                     | <span data-ttu-id="c21c3-262">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-262">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-263">TotalDiscountPercentOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-263">TotalDiscountPercentOperationRequest</span></span>            |  <span data-ttu-id="c21c3-264">トランザクションへ合計割引率を追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-264">Add total discount percent to the transaction.</span></span>                                         | <span data-ttu-id="c21c3-265">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-265">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-266">VoidCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-266">VoidCartLineOperationRequest</span></span>                    |  <span data-ttu-id="c21c3-267">買い物カゴ明細行を無効にします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-267">Voids the cart line.</span></span>                                      | <span data-ttu-id="c21c3-268">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-268">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-269">VoidTenderLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-269">VoidTenderLineOperationRequest</span></span>                  | <span data-ttu-id="c21c3-270">入金明細行を無効にします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-270">Voids the tender line.</span></span>                                       | <span data-ttu-id="c21c3-271">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-271">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-272">VoidTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-272">VoidTransactionOperationRequest</span></span>                 |  <span data-ttu-id="c21c3-273">トランザクションを無効にします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-273">Voids the transaction.</span></span>                                      | <span data-ttu-id="c21c3-274">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-274">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-275">CreateEmptyCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-275">CreateEmptyCartServiceRequest</span></span>                   |  <span data-ttu-id="c21c3-276">空の買い物カゴを作成します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-276">Creates empty cart.</span></span>                                      | <span data-ttu-id="c21c3-277">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-277">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-278">GetTaxOverridesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-278">GetTaxOverridesServiceRequest</span></span>                   |  <span data-ttu-id="c21c3-279">税の上書きの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-279">Gets the tax override list.</span></span>                                      | <span data-ttu-id="c21c3-280">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-280">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-281">UpdateTenderLineSignatureServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-281">UpdateTenderLineSignatureServiceRequest</span></span>         |  <span data-ttu-id="c21c3-282">入金明細行の署名データを更新します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-282">Updates the tender line signature data.</span></span>                                      | <span data-ttu-id="c21c3-283">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-283">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-284">CarryoutSelectedProductsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-284">CarryoutSelectedProductsOperationRequest</span></span> |   <span data-ttu-id="c21c3-285">選択した明細行を実行としてマークします。</span><span class="sxs-lookup"><span data-stu-id="c21c3-285">Marks the selected line as carry out.</span></span>                                            | <span data-ttu-id="c21c3-286">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-286">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-287">AddCouponsOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-287">AddCouponsOperationRequest</span></span> |    <span data-ttu-id="c21c3-288">トランザクションにクーポンを追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-288">Add coupon to the transaction.</span></span>                                                         | <span data-ttu-id="c21c3-289">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-289">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-290">CreateNonSalesTransactionServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-290">CreateNonSalesTransactionServiceRequest</span></span> | <span data-ttu-id="c21c3-291">販売以外のトランザクションの買い物カゴを作成します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-291">Create non sales transaction cart.</span></span>                                               | <span data-ttu-id="c21c3-292">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-292">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-293">ReturnTransactionOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-293">ReturnTransactionOperationRequest</span></span> |  <span data-ttu-id="c21c3-294">トランザクションを返します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-294">Returns the transaction.</span></span>                                                    | <span data-ttu-id="c21c3-295">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-295">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-296">AddLoyaltyCardToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-296">AddLoyaltyCardToCartOperationRequest</span></span> | <span data-ttu-id="c21c3-297">ロイヤルティ カードをトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-297">Adds loyalty card to the transaction.</span></span>                                                  | <span data-ttu-id="c21c3-298">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-298">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-299">ReturnCartLineOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-299">ReturnCartLineOperationRequest</span></span> |   <span data-ttu-id="c21c3-300">買い物カゴ明細行を返します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-300">Returns the cart line.</span></span>                                                      | <span data-ttu-id="c21c3-301">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-301">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-302">ReturnItemOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-302">ReturnItemOperationRequest</span></span> |  <span data-ttu-id="c21c3-303">品目を返します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-303">Returns the item.</span></span>                                                           | <span data-ttu-id="c21c3-304">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-304">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-305">AddExpenseAccountLineToCartOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-305">AddExpenseAccountLineToCartOperationRequest</span></span> | <span data-ttu-id="c21c3-306">経費勘定明細行を買い物カゴに追加します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-306">Add expense account line to the cart.</span></span>                                           | <span data-ttu-id="c21c3-307">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-307">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-308">ShipAllCartLinesOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-308">ShipAllCartLinesOperationRequest</span></span> |   <span data-ttu-id="c21c3-309">買い物カゴのすべての明細行を出荷します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-309">Ships all the cart lines.</span></span>                                                    | <span data-ttu-id="c21c3-310">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-310">10.0.14</span></span>  |
| <span data-ttu-id="c21c3-311">ShipSelectedCartLinesOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-311">ShipSelectedCartLinesOperationRequest</span></span> |    <span data-ttu-id="c21c3-312">買い物カゴの選択した明細行を出荷します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-312">Ships the selected cart line.</span></span>                                              | <span data-ttu-id="c21c3-313">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-313">10.0.14</span></span>  |
|<span data-ttu-id="c21c3-314">PickupSelectedOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-314">PickupSelectedOperationRequest</span></span> | <span data-ttu-id="c21c3-315">含められた明細行を出荷対象としてマークする</span><span class="sxs-lookup"><span data-stu-id="c21c3-315">Marks the included lines for pickup</span></span>                      |  <span data-ttu-id="c21c3-316">10.0.16</span><span class="sxs-lookup"><span data-stu-id="c21c3-316">10.0.16</span></span> |


### <a name="payments"></a><span data-ttu-id="c21c3-317">支払利息</span><span class="sxs-lookup"><span data-stu-id="c21c3-317">Payments</span></span>

<span data-ttu-id="c21c3-318">次の表に、支払に関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-318">The following table lists APIs exposed to perform payment-related functionality.</span></span>

| <span data-ttu-id="c21c3-319">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-319">POS API</span></span>                                   | <span data-ttu-id="c21c3-320">説明</span><span class="sxs-lookup"><span data-stu-id="c21c3-320">Description</span></span>                            | <span data-ttu-id="c21c3-321">リリース</span><span class="sxs-lookup"><span data-stu-id="c21c3-321">Release</span></span>                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| <span data-ttu-id="c21c3-322">GetGiftCardByIdServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-322">GetGiftCardByIdServiceRequest</span></span>             | <span data-ttu-id="c21c3-323">ギフト カード ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-323">Gets the gift card ID.</span></span>     |   <span data-ttu-id="c21c3-324">10.0.12</span><span class="sxs-lookup"><span data-stu-id="c21c3-324">10.0.12</span></span>   |
| <span data-ttu-id="c21c3-325">GetPaymentCardTypeByBinRangeClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-325">GetPaymentCardTypeByBinRangeClientRequest</span></span> | <span data-ttu-id="c21c3-326">カード タイプの BIN 範囲を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-326">Get the card type bin range.</span></span>  |  <span data-ttu-id="c21c3-327">10.0.12</span><span class="sxs-lookup"><span data-stu-id="c21c3-327">10.0.12</span></span>     |
| <span data-ttu-id="c21c3-328">GetSignatureClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-328">GetSignatureClientRequest</span></span>                 | <span data-ttu-id="c21c3-329">署名のキャプチャ ダイアログを POS で表示するか、またはコンフィギュレーションに基づいてメッセージを署名キャプチャ デバイスに送信します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-329">Shows the signature capture dialog in POS or sends the message to the signature capture device based on the configuration.</span></span> | <span data-ttu-id="c21c3-330">10.0.15</span><span class="sxs-lookup"><span data-stu-id="c21c3-330">10.0.15</span></span> |

### <a name="peripherals"></a><span data-ttu-id="c21c3-331">周辺機器</span><span class="sxs-lookup"><span data-stu-id="c21c3-331">Peripherals</span></span>

<span data-ttu-id="c21c3-332">次の表に、周辺機器に関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-332">The following table lists APIs exposed to perform peripheral-related functionality.</span></span>

| <span data-ttu-id="c21c3-333">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-333">POS API</span></span>                                                |
|--------------------------------------------------------|
| <span data-ttu-id="c21c3-334">CardPaymentAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-334">CardPaymentAuthorizePaymentRequest</span></span>                     |
| <span data-ttu-id="c21c3-335">CardPaymentBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-335">CardPaymentBeginTransactionRequest</span></span>                     |
| <span data-ttu-id="c21c3-336">CardPaymentCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-336">CardPaymentCapturePaymentRequest</span></span>                       |
| <span data-ttu-id="c21c3-337">CardPaymentEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-337">CardPaymentEndTransactionRequest</span></span>                       |
| <span data-ttu-id="c21c3-338">CardPaymentEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-338">CardPaymentEnquireGiftCardBalancePeripheralRequest</span></span>     |
| <span data-ttu-id="c21c3-339">CardPaymentExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-339">CardPaymentExecuteTaskRequest</span></span>                          |
| <span data-ttu-id="c21c3-340">CardPaymentRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-340">CardPaymentRefundPaymentRequest</span></span>                        |
| <span data-ttu-id="c21c3-341">CardPaymentVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-341">CardPaymentVoidPaymentRequest</span></span>                          |
| <span data-ttu-id="c21c3-342">CardPaymentAuthorizeCardTokenPeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-342">CardPaymentAuthorizeCardTokenPeripheralRequest</span></span>                          |
| <span data-ttu-id="c21c3-343">CashDrawerIsOpenRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-343">CashDrawerIsOpenRequest</span></span>                                |
| <span data-ttu-id="c21c3-344">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-344">HardwareStationDeviceActionRequest</span></span>                     |
| <span data-ttu-id="c21c3-345">HardwareStationStatusRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-345">HardwareStationStatusRequest</span></span>                           |
| <span data-ttu-id="c21c3-346">LineDisplayDisplayLinesRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-346">LineDisplayDisplayLinesRequest</span></span>                         |
| <span data-ttu-id="c21c3-347">PaymentTerminalAuthorizePaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-347">PaymentTerminalAuthorizePaymentActivityRequest</span></span>         |
| <span data-ttu-id="c21c3-348">PaymentTerminalAuthorizePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-348">PaymentTerminalAuthorizePaymentRequest</span></span>                 |
| <span data-ttu-id="c21c3-349">PaymentTerminalBeginTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-349">PaymentTerminalBeginTransactionRequest</span></span>                 |
| <span data-ttu-id="c21c3-350">PaymentTerminalCancelOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-350">PaymentTerminalCancelOperationRequest</span></span>                  |
| <span data-ttu-id="c21c3-351">PaymentTerminalCapturePaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-351">PaymentTerminalCapturePaymentRequest</span></span>                   |
| <span data-ttu-id="c21c3-352">PaymentTerminalEndTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-352">PaymentTerminalEndTransactionRequest</span></span>                   |
| <span data-ttu-id="c21c3-353">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-353">PaymentTerminalEnquireGiftCardBalancePeripheralRequest</span></span> |
| <span data-ttu-id="c21c3-354">PaymentTerminalExecuteTaskRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-354">PaymentTerminalExecuteTaskRequest</span></span>                      |
| <span data-ttu-id="c21c3-355">PaymentTerminalRefundPaymentActivityRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-355">PaymentTerminalRefundPaymentActivityRequest</span></span>            |
| <span data-ttu-id="c21c3-356">PaymentTerminalRefundPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-356">PaymentTerminalRefundPaymentRequest</span></span>                    |
| <span data-ttu-id="c21c3-357">PaymentTerminalUpdateLinesRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-357">PaymentTerminalUpdateLinesRequest</span></span>                      |
| <span data-ttu-id="c21c3-358">PaymentTerminalVoidPaymentRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-358">PaymentTerminalVoidPaymentRequest</span></span>                      |
| <span data-ttu-id="c21c3-359">PaymentTerminalFetchTokenPeripheralRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-359">PaymentTerminalFetchTokenPeripheralRequest</span></span>             |
| <span data-ttu-id="c21c3-360">PrinterPrintRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-360">PrinterPrintRequest</span></span>                                    |
| <span data-ttu-id="c21c3-361">ScaleReadRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-361">ScaleReadRequest</span></span>                                       |

### <a name="scanresults"></a><span data-ttu-id="c21c3-362">ScanResults</span><span class="sxs-lookup"><span data-stu-id="c21c3-362">ScanResults</span></span>

<span data-ttu-id="c21c3-363">次の表に、スキャン結果に関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-363">The following table lists APIs exposed to perform scan results-related functionality.</span></span>

| <span data-ttu-id="c21c3-364">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-364">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="c21c3-365">GetScanResultClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-365">GetScanResultClientRequest</span></span> |

### <a name="customer"></a><span data-ttu-id="c21c3-366">顧客</span><span class="sxs-lookup"><span data-stu-id="c21c3-366">Customer</span></span>

<span data-ttu-id="c21c3-367">次の表に、顧客に関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-367">The following table lists APIs exposed to perform customer-related functionality.</span></span>

| <span data-ttu-id="c21c3-368">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-368">POS API</span></span>                  |
|--------------------------|
| <span data-ttu-id="c21c3-369">GetCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-369">GetCustomerClientRequest</span></span> |
|<span data-ttu-id="c21c3-370">CreateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-370">CreateCustomerServiceRequest</span></span> |
|<span data-ttu-id="c21c3-371">UpdateCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-371">UpdateCustomerServiceRequest</span></span> |
|<span data-ttu-id="c21c3-372">SelectCustomerClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-372">SelectCustomerClientRequest</span></span> |


### <a name="authentication"></a><span data-ttu-id="c21c3-373">認証</span><span class="sxs-lookup"><span data-stu-id="c21c3-373">Authentication</span></span>

<span data-ttu-id="c21c3-374">次の表に、承認に関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-374">The following table lists APIs exposed to perform authentication-related functionality.</span></span>

| <span data-ttu-id="c21c3-375">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-375">POS API</span></span>                |
|------------------------|
| <span data-ttu-id="c21c3-376">LogOffOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-376">LogOffOperationRequest</span></span> |
| <span data-ttu-id="c21c3-377">LockRegisterOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-377">LockRegisterOperationRequest</span></span> |

### <a name="dataservice"></a><span data-ttu-id="c21c3-378">DataService</span><span class="sxs-lookup"><span data-stu-id="c21c3-378">DataService</span></span>

<span data-ttu-id="c21c3-379">次の表に、データ サービスに関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-379">The following table lists APIs exposed to perform data service-related functionality.</span></span>

| <span data-ttu-id="c21c3-380">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-380">POS API</span></span>            |
|--------------------|
| <span data-ttu-id="c21c3-381">DataServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-381">DataServiceRequest</span></span> |

### <a name="device"></a><span data-ttu-id="c21c3-382">デバイス</span><span class="sxs-lookup"><span data-stu-id="c21c3-382">Device</span></span>

<span data-ttu-id="c21c3-383">次の表に、デバイスに関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-383">The following table lists APIs exposed to perform device-related functionality.</span></span>

| <span data-ttu-id="c21c3-384">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-384">POS API</span></span>                               |
|---------------------------------------|
| <span data-ttu-id="c21c3-385">GetDeviceConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-385">GetDeviceConfigurationClientRequest</span></span>   |
| <span data-ttu-id="c21c3-386">GetExtensionProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-386">GetExtensionProfileClientRequest</span></span>      |
| <span data-ttu-id="c21c3-387">GetHardwareProfileClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-387">GetHardwareProfileClientRequest</span></span>       |
| <span data-ttu-id="c21c3-388">GetAuthenticationTokenClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-388">GetAuthenticationTokenClientRequest</span></span>   |
| <span data-ttu-id="c21c3-389">GetConnectionStatusClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-389">GetConnectionStatusClientRequest</span></span>      |
| <span data-ttu-id="c21c3-390">GetActiveHardwareStationClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-390">GetActiveHardwareStationClientRequest</span></span> |
| <span data-ttu-id="c21c3-391">GetApplicationVersionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-391">GetApplicationVersionClientRequest</span></span>    |
| <span data-ttu-id="c21c3-392">GetChannelConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-392">GetChannelConfigurationClientRequest</span></span>  |

### <a name="diagnostics"></a><span data-ttu-id="c21c3-393">診断</span><span class="sxs-lookup"><span data-stu-id="c21c3-393">Diagnostics</span></span> 

<span data-ttu-id="c21c3-394">次の表に、診断に関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-394">The following table lists APIs exposed to perform diagnostics-related functionality.</span></span>

| <span data-ttu-id="c21c3-395">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-395">POS API</span></span>                     |
|-----------------------------|
| <span data-ttu-id="c21c3-396">GetSessionInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-396">GetSessionInfoClientRequest</span></span> |

### <a name="dialog"></a><span data-ttu-id="c21c3-397">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="c21c3-397">Dialog</span></span>

<span data-ttu-id="c21c3-398">次の表に、ダイアログに関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-398">The following table lists APIs exposed to perform dialog-related functionality.</span></span>

| <span data-ttu-id="c21c3-399">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-399">POS API</span></span>                                  |
|------------------------------------------|
| <span data-ttu-id="c21c3-400">ShowMessageDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-400">ShowMessageDialogClientRequest</span></span>           |
| <span data-ttu-id="c21c3-401">IAlphanumericInputDialogResult</span><span class="sxs-lookup"><span data-stu-id="c21c3-401">IAlphanumericInputDialogResult</span></span>           |
| <span data-ttu-id="c21c3-402">ShowAlphanumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-402">ShowAlphanumericInputDialogClientRequest</span></span> |
| <span data-ttu-id="c21c3-403">ShowNumericInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-403">ShowNumericInputDialogClientRequest</span></span>      |
| <span data-ttu-id="c21c3-404">ShowListInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-404">ShowListInputDialogClientRequest</span></span>         |
| <span data-ttu-id="c21c3-405">ShowTextInputDialogClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-405">ShowTextInputDialogClientRequest</span></span>         |

### <a name="employee"></a><span data-ttu-id="c21c3-406">従業員</span><span class="sxs-lookup"><span data-stu-id="c21c3-406">Employee</span></span>

<span data-ttu-id="c21c3-407">次の表に、従業員に関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-407">The following table lists APIs exposed to perform employee-related functionality.</span></span>

| <span data-ttu-id="c21c3-408">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-408">POS API</span></span>                                   | <span data-ttu-id="c21c3-409">説明</span><span class="sxs-lookup"><span data-stu-id="c21c3-409">Description</span></span>                            | <span data-ttu-id="c21c3-410">リリース</span><span class="sxs-lookup"><span data-stu-id="c21c3-410">Release</span></span>                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| <span data-ttu-id="c21c3-411">GetLoggedOnEmployeeClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-411">GetLoggedOnEmployeeClientRequest</span></span> |  <span data-ttu-id="c21c3-412">現在 POS にログインしている従業員の詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-412">Gets the current logged in POS employee details.</span></span>      | <span data-ttu-id="c21c3-413">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-413">10.0.14</span></span>      |
| <span data-ttu-id="c21c3-414">SelectStoreEmployeeClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-414">SelectStoreEmployeeClientRequest</span></span> | <span data-ttu-id="c21c3-415">現在の店舗の選択可能な従業員の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-415">Gets the current store employee list for selection.</span></span> | <span data-ttu-id="c21c3-416">10.0.16</span><span class="sxs-lookup"><span data-stu-id="c21c3-416">10.0.16</span></span> |

### <a name="formatters"></a><span data-ttu-id="c21c3-417">フォーマッター</span><span class="sxs-lookup"><span data-stu-id="c21c3-417">Formatters</span></span>

<span data-ttu-id="c21c3-418">次の表に、フォーマッターに関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-418">The following table lists APIs exposed to perform formatter-related functionality.</span></span>

| <span data-ttu-id="c21c3-419">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-419">POS API</span></span>                             |
|-------------------------------------|
| <span data-ttu-id="c21c3-420">IBooleanFormatter</span><span class="sxs-lookup"><span data-stu-id="c21c3-420">IBooleanFormatter</span></span>                   |
| <span data-ttu-id="c21c3-421">ICurrencyFormatter</span><span class="sxs-lookup"><span data-stu-id="c21c3-421">ICurrencyFormatter</span></span>                  |
| <span data-ttu-id="c21c3-422">IDateFormatter</span><span class="sxs-lookup"><span data-stu-id="c21c3-422">IDateFormatter</span></span>                      |
| <span data-ttu-id="c21c3-423">ITransactionTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="c21c3-423">ITransactionTypeFormatter</span></span>           |
| <span data-ttu-id="c21c3-424">IPurchaseTransferOrderTypeFormatter</span><span class="sxs-lookup"><span data-stu-id="c21c3-424">IPurchaseTransferOrderTypeFormatter</span></span> |

### <a name="orgunits"></a><span data-ttu-id="c21c3-425">OrgUnits</span><span class="sxs-lookup"><span data-stu-id="c21c3-425">OrgUnits</span></span>

<span data-ttu-id="c21c3-426">次の表に、組織単位に関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-426">The following table lists APIs exposed to perform org units-related functionality.</span></span>

| <span data-ttu-id="c21c3-427">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-427">POS API</span></span>                              |
|--------------------------------------|
| <span data-ttu-id="c21c3-428">GetOrgUnitConfigurationClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-428">GetOrgUnitConfigurationClientRequest</span></span> |
| <span data-ttu-id="c21c3-429">GetOrgUnitTenderTypesClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-429">GetOrgUnitTenderTypesClientRequest</span></span>   |
| <span data-ttu-id="c21c3-430">InventoryLookupOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-430">InventoryLookupOperationRequest</span></span>      |

### <a name="products"></a><span data-ttu-id="c21c3-431">製品</span><span class="sxs-lookup"><span data-stu-id="c21c3-431">Products</span></span>

<span data-ttu-id="c21c3-432">次の表に、製品に関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-432">The following table lists APIs exposed to perform products-related functionality.</span></span>

| <span data-ttu-id="c21c3-433">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-433">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="c21c3-434">GetProductsByIdsClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-434">GetProductsByIdsClientRequest</span></span>              |
| <span data-ttu-id="c21c3-435">GetCurrentProductCatalogStoreClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-435">GetCurrentProductCatalogStoreClientRequest</span></span> |
| <span data-ttu-id="c21c3-436">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-436">SelectProductVariantClientRequest</span></span>          |
| <span data-ttu-id="c21c3-437">GetSerialNumberClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-437">GetSerialNumberClientRequest</span></span>               |
| <span data-ttu-id="c21c3-438">GetRefinerValuesByTextServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-438">GetRefinerValuesByTextServiceRequest</span></span>       |
| <span data-ttu-id="c21c3-439">SelectProductClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-439">SelectProductClientRequest</span></span> |
| <span data-ttu-id="c21c3-440">SelectProductVariantClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-440">SelectProductVariantClientRequest</span></span> |
| <span data-ttu-id="c21c3-441">GetActivePricesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-441">GetActivePricesServiceRequest</span></span> |

### <a name="categories"></a><span data-ttu-id="c21c3-442">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="c21c3-442">Categories</span></span>

<span data-ttu-id="c21c3-443">次の表に、カテゴリに関連する機能を実行できる公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-443">The following table lists APIs exposed to perform categories-related functionality.</span></span>

| <span data-ttu-id="c21c3-444">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-444">POS API</span></span>                                    |
|--------------------------------------------|
| <span data-ttu-id="c21c3-445">GetCategoriesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-445">GetCategoriesServiceRequest</span></span>              |


### <a name="salesorders"></a><span data-ttu-id="c21c3-446">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="c21c3-446">SalesOrders</span></span>

<span data-ttu-id="c21c3-447">次の表に、販売注文に関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-447">The following table lists APIs exposed to perform sales orders-related functionality.</span></span>

| <span data-ttu-id="c21c3-448">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-448">POS API</span></span>                                          |
|--------------------------------------------------|
| <span data-ttu-id="c21c3-449">GetReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-449">GetReceiptsClientRequest</span></span>                         |
| <span data-ttu-id="c21c3-450">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-450">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="c21c3-451">GetSalesOrderDetailsByTransactionIdClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-451">GetSalesOrderDetailsByTransactionIdClientRequest</span></span> |
| <span data-ttu-id="c21c3-452">GetGiftReceiptsClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-452">GetGiftReceiptsClientRequest</span></span>                     |
| <span data-ttu-id="c21c3-453">RegisterPrintReceiptCopyEventRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-453">RegisterPrintReceiptCopyEventRequest</span></span>             |
| <span data-ttu-id="c21c3-454">MarkAsPickedServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-454">MarkAsPickedServiceRequest</span></span>                       |
| <span data-ttu-id="c21c3-455">PrintPackingSlipClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-455">PrintPackingSlipClientRequest</span></span>                    |
| <span data-ttu-id="c21c3-456">PickUpCustomerOrderLinesClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-456">PickUpCustomerOrderLinesClientRequest</span></span>            |


### <a name="shifts"></a><span data-ttu-id="c21c3-457">シフト</span><span class="sxs-lookup"><span data-stu-id="c21c3-457">Shifts</span></span>

<span data-ttu-id="c21c3-458">次の表に、シフトに関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-458">The following table lists APIs exposed to perform shifts-related functionality.</span></span>

| <span data-ttu-id="c21c3-459">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-459">POS API</span></span>                    |
|----------------------------|
| <span data-ttu-id="c21c3-460">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-460">CloseShiftOperationRequest</span></span> |
| <span data-ttu-id="c21c3-461">CloseShiftOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-461">CloseShiftOperationRequest</span></span> |

### <a name="stockcountjournals"></a><span data-ttu-id="c21c3-462">StockCountJournals</span><span class="sxs-lookup"><span data-stu-id="c21c3-462">StockCountJournals</span></span>

<span data-ttu-id="c21c3-463">次の表に、在庫数仕訳帳に関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-463">The following table lists APIs exposed to perform stock count journals-related functionality.</span></span>

| <span data-ttu-id="c21c3-464">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-464">POS API</span></span>                                |
|----------------------------------------|
| <span data-ttu-id="c21c3-465">SyncAllStockCountJournalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-465">SyncAllStockCountJournalsClientRequest</span></span> |

### <a name="storeoperations"></a><span data-ttu-id="c21c3-466">StoreOperations</span><span class="sxs-lookup"><span data-stu-id="c21c3-466">StoreOperations</span></span>

<span data-ttu-id="c21c3-467">次の表に、店舗運営に関連する機能を実行する公開済みの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-467">The following table lists APIs exposed to perform store operations-related functionality.</span></span>

| <span data-ttu-id="c21c3-468">POS API</span><span class="sxs-lookup"><span data-stu-id="c21c3-468">POS API</span></span>                                   | <span data-ttu-id="c21c3-469">説明</span><span class="sxs-lookup"><span data-stu-id="c21c3-469">Description</span></span>                            | <span data-ttu-id="c21c3-470">リリース</span><span class="sxs-lookup"><span data-stu-id="c21c3-470">Release</span></span>                  |
|-------------------------------------------|----------------------------------------|--------------------------|
| <span data-ttu-id="c21c3-471">DeclareStartingAmountClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-471">DeclareStartingAmountClientRequest</span></span>              | <span data-ttu-id="c21c3-472">この要求を使用して開始金額を申告します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-472">Declare start amount using this request.</span></span> | <span data-ttu-id="c21c3-473">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-473">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-474">GetSalesOrdersWithNoFiscalTransactionsRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-474">GetSalesOrdersWithNoFiscalTransactionsRequest</span></span>   | <span data-ttu-id="c21c3-475">会計トランザクション要求のない販売注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-475">Gets sales order with no fiscal transaction request.</span></span>  |   <span data-ttu-id="c21c3-476">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-476">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-477">RegisterCustomAuditEventClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-477">RegisterCustomAuditEventClientRequest</span></span>           | <span data-ttu-id="c21c3-478">カスタム監査イベント要求を登録します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-478">Register custom audit event request.</span></span>   |  <span data-ttu-id="c21c3-479">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-479">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-480">GetOfflinePendingTransactionCountClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-480">GetOfflinePendingTransactionCountClientRequest</span></span>  | <span data-ttu-id="c21c3-481">オフラインで保留中のトランザクション カウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-481">Gets the offline pending transaction count.</span></span>  | <span data-ttu-id="c21c3-482">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-482">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-483">SaveFiscalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-483">SaveFiscalTransactionClientRequest</span></span>              | <span data-ttu-id="c21c3-484">会計トランザクション要求を保存します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-484">Save fiscal transaction request.</span></span>   |   <span data-ttu-id="c21c3-485">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-485">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-486">SafeDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-486">SafeDropOperationRequest</span></span>                        | <span data-ttu-id="c21c3-487">金庫保管操作要求。</span><span class="sxs-lookup"><span data-stu-id="c21c3-487">Safe drop operation request.</span></span>  |  <span data-ttu-id="c21c3-488">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-488">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-489">TenderDeclarationOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-489">TenderDeclarationOperationRequest</span></span>               | <span data-ttu-id="c21c3-490">入金申告操作要求。</span><span class="sxs-lookup"><span data-stu-id="c21c3-490">Tender declaration operation request.</span></span>      |   <span data-ttu-id="c21c3-491">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-491">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-492">TenderRemovalOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-492">TenderRemovalOperationRequest</span></span>                   | <span data-ttu-id="c21c3-493">入金削除操作要求。</span><span class="sxs-lookup"><span data-stu-id="c21c3-493">Tender removal operation request.</span></span>  |  <span data-ttu-id="c21c3-494">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-494">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-495">CreateBankDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-495">CreateBankDropTransactionClientRequest</span></span>          | <span data-ttu-id="c21c3-496">銀行入金トランザクション要求。</span><span class="sxs-lookup"><span data-stu-id="c21c3-496">Bank drop transaction request.</span></span>    | <span data-ttu-id="c21c3-497">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-497">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-498">CreateFloatEntryTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-498">CreateFloatEntryTransactionClientRequest</span></span>        | <span data-ttu-id="c21c3-499">釣銭入力トランザクション要求。</span><span class="sxs-lookup"><span data-stu-id="c21c3-499">Float entry transaction request.</span></span> |  <span data-ttu-id="c21c3-500">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-500">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-501">CreateStartingAmountTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-501">CreateStartingAmountTransactionClientRequest</span></span>    | <span data-ttu-id="c21c3-502">開始金額トランザクション要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-502">Create start amount transaction request.</span></span>       |   <span data-ttu-id="c21c3-503">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-503">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-504">CreateTenderDeclarationTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-504">CreateTenderDeclarationTransactionClientRequest</span></span> | <span data-ttu-id="c21c3-505">入金申告トランザクション要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-505">Create tender declaration transaction request.</span></span>     |   <span data-ttu-id="c21c3-506">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-506">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-507">CreateTenderRemovalTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-507">CreateTenderRemovalTransactionClientRequest</span></span>     | <span data-ttu-id="c21c3-508">入金申告トランザクション要求を削除します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-508">Remove tender declaration transaction request.</span></span>       |  <span data-ttu-id="c21c3-509">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-509">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-510">GetDenominationTotalsClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-510">GetDenominationTotalsClientRequest</span></span>              | <span data-ttu-id="c21c3-511">単位合計要求を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-511">Gets the denomination total request.</span></span>        | <span data-ttu-id="c21c3-512">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-512">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-513">SelectZipCodeInfoClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-513">SelectZipCodeInfoClientRequest</span></span>                  | <span data-ttu-id="c21c3-514">郵便番号情報の要求を選択します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-514">Selects the Zip code information request.</span></span>    | <span data-ttu-id="c21c3-515">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-515">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-516">CreateSafeDropTransactionClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-516">CreateSafeDropTransactionClientRequest</span></span>          | <span data-ttu-id="c21c3-517">金庫保管トランザクション要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-517">Create safe drop transaction request.</span></span>                                       |  <span data-ttu-id="c21c3-518">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-518">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-519">GetTenderDetailsClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-519">GetTenderDetailsClientRequest</span></span>                   | <span data-ttu-id="c21c3-520">入金の詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-520">Gets the tender details.</span></span>    | <span data-ttu-id="c21c3-521">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-521">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-522">LoyaltyCardPointsBalanceOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-522">LoyaltyCardPointsBalanceOperationRequest</span></span>        | <span data-ttu-id="c21c3-523">ロイヤルティ カードの残高を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-523">Gets the loyalty card balance.</span></span>  | <span data-ttu-id="c21c3-524">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-524">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-525">GetCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-525">GetCommissionSalesGroupsServiceRequest</span></span>          | <span data-ttu-id="c21c3-526">コミッション売上グループを取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-526">Gets the commission sales group.</span></span>  |  <span data-ttu-id="c21c3-527">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-527">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-528">GetCurrenciesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-528">GetCurrenciesServiceRequest</span></span>                     | <span data-ttu-id="c21c3-529">店舗の通貨を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-529">Gets the store currencies.</span></span> | <span data-ttu-id="c21c3-530">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-530">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-531">GetSrsReportDataSetServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-531">GetSrsReportDataSetServiceRequest</span></span>               | <span data-ttu-id="c21c3-532">SRS レポート データを取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-532">Gets the Srs report data.</span></span>  |  <span data-ttu-id="c21c3-533">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-533">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-534">SearchCommissionSalesGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-534">SearchCommissionSalesGroupsServiceRequest</span></span>       |  <span data-ttu-id="c21c3-535">コミッション売上グループの要求を検索します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-535">Search commission sales groups request.</span></span>   | <span data-ttu-id="c21c3-536">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-536">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-537">IssueLoyaltyCardOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-537">IssueLoyaltyCardOperationRequest</span></span>                |  <span data-ttu-id="c21c3-538">ロイヤルティ カードを発行します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-538">Issues loyalty card.</span></span>  |  <span data-ttu-id="c21c3-539">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-539">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-540">GetPickingAndReceivingOrdersClientRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-540">GetPickingAndReceivingOrdersClientRequest</span></span>       |  <span data-ttu-id="c21c3-541">ピッキングと入荷の注文リストを取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-541">Gets the picking and receiving orders list.</span></span>  |    <span data-ttu-id="c21c3-542">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-542">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-543">BankDropOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-543">BankDropOperationRequest</span></span>                 |  <span data-ttu-id="c21c3-544">銀行入金要求。</span><span class="sxs-lookup"><span data-stu-id="c21c3-544">Bank drop request.</span></span>   |        <span data-ttu-id="c21c3-545">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-545">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-546">DeclareStartAmountOperationRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-546">DeclareStartAmountOperationRequest</span></span>        |   <span data-ttu-id="c21c3-547">開始金額申告要求。</span><span class="sxs-lookup"><span data-stu-id="c21c3-547">Declare start amount request.</span></span>       |          <span data-ttu-id="c21c3-548">10.0.14</span><span class="sxs-lookup"><span data-stu-id="c21c3-548">10.0.14</span></span>        |
| <span data-ttu-id="c21c3-549">GetAllDiscountsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="c21c3-549">GetAllDiscountsServiceRequest</span></span>        | <span data-ttu-id="c21c3-550">現在の買い物カゴに適用できる割引を取得します。</span><span class="sxs-lookup"><span data-stu-id="c21c3-550">Gets the discount applicable for the current cart.</span></span>  | <span data-ttu-id="c21c3-551">10.0.16</span><span class="sxs-lookup"><span data-stu-id="c21c3-551">10.0.16</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]