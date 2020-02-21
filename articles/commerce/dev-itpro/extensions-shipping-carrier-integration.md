---
title: 注文のフルフィルメント中の梱包明細の拡張ポイント
description: このトピックでは、カスタマイズを使用して、顧客注文の処理中に梱包明細に拡張ポイントを追加する方法を示します。
author: mugunthanm
manager: AnnBe
ms.date: 03/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-03-31
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: a6598212d1b1575a3580228d9c7dd3f8002852ba
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004574"
---
# <a name="extension-points-for-packing-slips-during-order-fulfillment"></a><span data-ttu-id="f17ba-103">注文のフルフィルメント中の梱包明細の拡張ポイント</span><span class="sxs-lookup"><span data-stu-id="f17ba-103">Extension points for packing slips during order fulfillment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f17ba-104">販売時点管理 (POS) から顧客注文の梱包明細を生成するとき、梱包明細に品目の重量を印刷する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f17ba-104">When you generate packing slips for customer orders from the point of sale (POS), you might want to print the item weight on the packing slip.</span></span> <span data-ttu-id="f17ba-105">パッケージについてのカスタム情報、送料に関して配送業者を呼び出す方法に関する情報、またはパッケージの返却方法についての情報を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-105">You might also want to add custom information about the package, information about how to call the shipping carrier for the shipping rates, or information about how to return the package.</span></span> <span data-ttu-id="f17ba-106">これらのシナリオを処理するため、受注処理のための梱包明細プロセスの延長ポイントが、バックオフィス、ビジネス ロジック層であるCommerce Runtime (CRT)、および POS で追加されました。</span><span class="sxs-lookup"><span data-stu-id="f17ba-106">To handle these scenarios, extension points for the packing slip process for order fulfillment have been added in Headquarters, in the commerce runtime (CRT), which is the business logic layer, and in the POS.</span></span> <span data-ttu-id="f17ba-107">これらの拡張ポイントを使用すると、拡張を介してカスタム フローとロジックを追加できます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-107">These extension points let you add custom flow and logic through extensions.</span></span>

## <a name="pos"></a><span data-ttu-id="f17ba-108">POS</span><span class="sxs-lookup"><span data-stu-id="f17ba-108">POS</span></span>
<span data-ttu-id="f17ba-109">POS では、**PrintPackingSlipClientRequestHandler** という名前の新しい要求ハンドラーで拡張機能をオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-109">In the POS, a new request handler that is named **PrintPackingSlipClientRequestHandler** lets you override extensions.</span></span> <span data-ttu-id="f17ba-110">この要求は、POS で**梱包明細を印刷する**ボタンを選択すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-110">This request is called when you select the **Print packing slip** button in the POS.</span></span> <span data-ttu-id="f17ba-111">この要求を上書きすることによって、POS でカスタム ロジックを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-111">By overriding this request, you can use custom logic in the POS.</span></span> <span data-ttu-id="f17ba-112">たとえば、独自の印刷メソッドを呼び出し、追加情報を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-112">For example, you can call your own printing methods and print additional information.</span></span>

<span data-ttu-id="f17ba-113">たとえば、既定では、PDF 形式で梱包明細を印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-113">For example, by default, you can print the packing slip in PDF format.</span></span> <span data-ttu-id="f17ba-114">POS クライアント要求を上書きすることによって、さまざまな形式で梱包明細を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-114">By overriding the POS client request, you can print the packing slip in a different format.</span></span> <span data-ttu-id="f17ba-115">または、特定の条件を確認し、基本的な条件に基づいて梱包明細の印刷、または印刷停止をすることができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-115">Alternatively, you can check for a specific condition, and then print or stop printing the packing slip, based on that condition.</span></span> <span data-ttu-id="f17ba-116">また、印刷前に検証を実行して、印刷ロジックまたはカスタム ロジックを止めることができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-116">You can also do validation before you print, and prevent printing or custom logic.</span></span> <span data-ttu-id="f17ba-117">ただし、印刷される実際のデータを変更する場合、CRT およびバックオフィスでビジネス ロジックを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f17ba-117">However, if you want to change the actual data that is printed, you must modify the business logic in CRT and Headquarters.</span></span>

### <a name="override-printpackingslipclientrequesthandler"></a><span data-ttu-id="f17ba-118">PrintPackingSlipClientRequestHandler のオーバーライド</span><span class="sxs-lookup"><span data-stu-id="f17ba-118">Override PrintPackingSlipClientRequestHandler</span></span>
<span data-ttu-id="f17ba-119">POS の要求をオーバーライドするには、POS で次のオーバーライド ハンドラー パターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-119">To override any request in the POS, use the following override handler pattern in the POS.</span></span>

<span data-ttu-id="f17ba-120">**例**</span><span class="sxs-lookup"><span data-stu-id="f17ba-120">**Example**</span></span>

```Typescript
import { PrintPackingSlipClientRequestHandler } from "PosApi/Extend/RequestHandlers/StoreFulfillmentRequestHandlers";
import { PrintPackingSlipClientRequest, PrintPackingSlipClientResponse } from "PosApi/Consume/SalesOrders";
import { ClientEntities } from "PosApi/Entities";
/**
 * Override request handler class for printing packing slip request.
 */
export default class PrintPackingSlipClientRequestHandlerExt extends PrintPackingSlipClientRequestHandler {
    /**
     * Executes the request handler asynchronously.
     * @param {PrintPackingSlipClientRequest<PrintPackingSlipClientResponse>} The request containing the response.
     * @return {Promise<ICancelableDataResult<PrintPackingSlipClientResponse>>} The cancelable promise containing the response.
     */
    public executeAsync(request: PrintPackingSlipClientRequest<PrintPackingSlipClientResponse>):
        Promise<ClientEntities.ICancelableDataResult<PrintPackingSlipClientResponse>> {
            // Do the extension logic here before calling the default handler.
            return this.defaultExecuteAsync(request);
        }
}
```

<span data-ttu-id="f17ba-121">要求を上書きした後は、新しい要求ハンドラー情報を含む manifest.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-121">After you override the request, update the manifest.json file with the new request handler information.</span></span>

```Typescript 
"requestHandlers": [
    {
        "modulePath": "Handlers/PrintPackingSlipClientRequestHandlerExt"
    }
]
```

## <a name="crt"></a><span data-ttu-id="f17ba-122">CRT</span><span class="sxs-lookup"><span data-stu-id="f17ba-122">CRT</span></span>
<span data-ttu-id="f17ba-123">POS クライアントの要求ハンドラーと同様、カスタム ロジックの拡張機能を有効にするため CRT に新しい要求が追加されました。</span><span class="sxs-lookup"><span data-stu-id="f17ba-123">Similar to the POS client request handler, new requests have been added in the CRT to enable extension of custom logic.</span></span>

### <a name="markaspickedrealtimerequest"></a><span data-ttu-id="f17ba-124">MarkAsPickedRealtimeRequest</span><span class="sxs-lookup"><span data-stu-id="f17ba-124">MarkAsPickedRealtimeRequest</span></span>
<span data-ttu-id="f17ba-125">**MarkAsPickedRealtimeRequest** 要求は、調達のための明細行をピッキング済みとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="f17ba-125">The **MarkAsPickedRealtimeRequest** request marks the fulfillment lines as picked.</span></span> <span data-ttu-id="f17ba-126">明細行がピッキング済みとマークされる前に、カスタム ロジックを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-126">You can add custom logic before the line is marked as picked.</span></span> <span data-ttu-id="f17ba-127">たとえば、プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-127">For example, you can change a property.</span></span> <span data-ttu-id="f17ba-128">後で、ピッキング済の明細行の情報が梱包明細の印刷に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-128">Later, the picked line information will be used to print the packing slip.</span></span> <span data-ttu-id="f17ba-129">シナリオに基づいて、この要求を無効にするか、プレトリガーまたはポストトリガーを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-129">Based on your scenario, you can override this request, or add pre-triggers or post-triggers.</span></span> 

<span data-ttu-id="f17ba-130">たとえば、 フルフィルメント明細行については、品目の重量などを計算します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-130">For example, for the fulfillment lines, you want to calculate item weight, and so on.</span></span> <span data-ttu-id="f17ba-131">この場合、サービスをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-131">In this case, you can customize the service.</span></span> 

> [!NOTE]
> <span data-ttu-id="f17ba-132">バックオフィスでカスタマイズを必要とするロジックを決定する必要がある場合、CRT でカスタマイズするのではなく、バックオフィス レベルでカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-132">If the logic that you require for your customization must be determined in Headquarters, you can customize at the Headquarters level instead of customizing in the CRT.</span></span> <span data-ttu-id="f17ba-133">たとえば、各明細行の品目重量を取得したいが、その情報はバックオフィスでのみ使用できる場合です。</span><span class="sxs-lookup"><span data-stu-id="f17ba-133">For example, if you want to get the item weight for each line, but that information is available only in Headquarters.</span></span> <span data-ttu-id="f17ba-134">この場合、関連するリアルタイム サービスのメソッドをカスタマイズしてから、バック オフィスから CRT に結果を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-134">In this case, you can customize the relevant real-time service methods and then return the result from Headquarters to the CRT.</span></span>

### <a name="packfulfillmentlinesrealtimerequest"></a><span data-ttu-id="f17ba-135">PackFulfillmentLinesRealtimeRequest</span><span class="sxs-lookup"><span data-stu-id="f17ba-135">PackFulfillmentLinesRealtimeRequest</span></span>
<span data-ttu-id="f17ba-136">**PackFulfillmentLinesRealtimeRequest** 要求は、フルフィルメント明細行のステータスを **部分的に梱包済み** または **梱包済み** に更新します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-136">The **PackFulfillmentLinesRealtimeRequest** request updates the status of the fulfillment lines to **Partially packed** or **Packed.**</span></span> <span data-ttu-id="f17ba-137">シナリオに基づいて、このサービスを無効にするか、プレトリガーまたはポストトリガーを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-137">Based on your scenario, you can override this service, or add pre-triggers or post-triggers.</span></span> 

## <a name="headquarters"></a><span data-ttu-id="f17ba-138">バックオフィス</span><span class="sxs-lookup"><span data-stu-id="f17ba-138">Headquarters</span></span>
<span data-ttu-id="f17ba-139">バックオフィスでは、梱包明細情報を取得して、拡張機能によってカスタム情報やロジックを追加するために、新しいリアルタイム サービス メソッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="f17ba-139">In Headquarters new real-time service methods have been added to get the packing slip information, and to add custom information or logic through extension.</span></span> <span data-ttu-id="f17ba-140">カスタマイズで、データまたはロジックがバックオフィスで実行されることを必須としている場合、拡張機能のパターンを使用して、これらのメソッドをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-140">If your customization requires that data or logic be done in Headquarters, you can customize these methods by using the extension patterns.</span></span> <span data-ttu-id="f17ba-141">また、取引サービス クライアント クラスを使用する拡張子シナリオが必要な場合は、CRT からこれらのメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-141">Additionally, if you require an extension scenario that uses the transaction service client class, you can call these methods from the CRT.</span></span>

### <a name="retailtransactionservicefulfillment"></a><span data-ttu-id="f17ba-142">RetailTransactionServiceFulfillment</span><span class="sxs-lookup"><span data-stu-id="f17ba-142">RetailTransactionServiceFulfillment</span></span>
<span data-ttu-id="f17ba-143">梱包明細プロセスに関連付けられているすべての新しいメソッドは注文のフルフィルメントにより、**RetailTransactionServiceFulfillment** クラスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-143">All the new methods that are related to the packing slip process for order fulfillment were added in the **RetailTransactionServiceFulfillment** class.</span></span>

### <a name="getpackingslipsdata"></a><span data-ttu-id="f17ba-144">GetPackingSlipsData</span><span class="sxs-lookup"><span data-stu-id="f17ba-144">GetPackingSlipsData</span></span>
<span data-ttu-id="f17ba-145">**GetPackingSlipsData** メソッドは、パラメーターとして販売 ID を渡すことによってすべての梱包明細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-145">The **GetPackingSlipsData** method returns all the packing slip information by passing the sales ID as a parameter.</span></span> 

### <a name="getfulfillmentlinesbypackingslipid"></a><span data-ttu-id="f17ba-146">GetFulfillmentLinesByPackingSlipId</span><span class="sxs-lookup"><span data-stu-id="f17ba-146">GetFulfillmentLinesByPackingSlipId</span></span>
<span data-ttu-id="f17ba-147">**GetFulfillmentLinesByPackingSlipId** メソッドは、梱包明細 ID に基づいて調達のための明細行を返します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-147">The **GetFulfillmentLinesByPackingSlipId** method returns the fulfillment lines, based on the packing slip ID.</span></span> <span data-ttu-id="f17ba-148">たとえば、梱包明細 ID があり、その梱包明細 ID に関連する販売明細行を取得する場合、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-148">For example, you can use this method if you have the packing slip ID, and you want to get the sales lines that are relevant to that packing slip ID.</span></span>

### <a name="markfulfillmentlinesaspacked"></a><span data-ttu-id="f17ba-149">MarkFulfillmentLinesAsPacked</span><span class="sxs-lookup"><span data-stu-id="f17ba-149">MarkFulfillmentLinesAsPacked</span></span>
<span data-ttu-id="f17ba-150">**MarkFulfillmentLinesAsPacked** メソッドは、調達のための詳細を XML 文字列形式でパラメーターとして取得することにより梱包される調達のための明細行のステータスを更新します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-150">The **MarkFulfillmentLinesAsPacked** method updates the status of the fulfillment lines to packed by taking the fulfillment details as a parameter in XML string format.</span></span> <span data-ttu-id="f17ba-151">POS は、POS ユーザー インターフェイス (UI) の選択した明細行をピッキング済としてマークするために CRT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-151">The POS calls the CRT to mark the selected lines from the POS user interface (UI) as picked.</span></span> <span data-ttu-id="f17ba-152">CRT の **MarkAsPickedRealtimeRequest** 要求がバックオフィスで **MarkFulfillmentLinesAsPacked** リアルタイム サービス メソッドを呼び出し、行のステータスを**梱包済み**として設定します。</span><span class="sxs-lookup"><span data-stu-id="f17ba-152">The **MarkAsPickedRealtimeRequest** request in the CRT then calls the **MarkFulfillmentLinesAsPacked** real-time service method in Headquarters to set the line status as **Packed**.</span></span>

<span data-ttu-id="f17ba-153">行が梱包済みとマークされていて印刷のために返された場合にカスタム ロジックを追加したり追加情報を返すには、**packingSlipExtensionPoint** メソッドをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-153">To add custom logic or return additional information when the line is marked as packed and returned for printing, you can customize the **packingSlipExtensionPoint** method.</span></span>

### <a name="packingslipextensionpoint"></a><span data-ttu-id="f17ba-154">packingSlipExtensionPoint</span><span class="sxs-lookup"><span data-stu-id="f17ba-154">packingSlipExtensionPoint</span></span>
<span data-ttu-id="f17ba-155">**packingSlipExtensionPoint** メソッドをカスタマイズして、カスタム ロジックを追加、または梱包明細 ID とともにカスタム情報を戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-155">You can customize the **packingSlipExtensionPoint** method to add custom logic or return custom information together with the packing slip ID.</span></span> <span data-ttu-id="f17ba-156">このカスタム情報には、梱包情報または納品書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f17ba-156">This custom information includes packing information or a delivery note.</span></span> <span data-ttu-id="f17ba-157">このメソッドは、通常、カスタム シナリオの拡張機能に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-157">This method is typically added for extensions for custom scenarios.</span></span> <span data-ttu-id="f17ba-158">このメソッドは、コマンド拡張ポイントのチェーンを使用して **MarkFulfillmentLinesAsPacked** メソッドから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-158">This method is called from the **MarkFulfillmentLinesAsPacked** method by using the chain of command extensibility point.</span></span> <span data-ttu-id="f17ba-159">**MarkFulfillmentLinesAsPacked** メソッドは、CRT コードが行うリアルタイム サービス呼び出しから実行されます。</span><span class="sxs-lookup"><span data-stu-id="f17ba-159">The **MarkFulfillmentLinesAsPacked** method is run from the real-time service call that the CRT code makes.</span></span>
