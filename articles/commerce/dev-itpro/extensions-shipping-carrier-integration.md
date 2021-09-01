---
title: 注文のフルフィルメント中の梱包明細の拡張ポイント
description: このトピックでは、カスタマイズを使用して、顧客注文の処理中に梱包明細に拡張ポイントを追加する方法を示します。
author: mugunthanm
ms.date: 03/29/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-03-31
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 49651179aea249266294c239fdd5c8d2b164a39bad48486c4e9f6df7d3cfe66a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733216"
---
# <a name="extension-points-for-packing-slips-during-order-fulfillment"></a>注文のフルフィルメント中の梱包明細の拡張ポイント

[!include [banner](../includes/banner.md)]

販売時点管理 (POS) から顧客注文の梱包明細を生成するとき、梱包明細に品目の重量を印刷する場合があります。 パッケージについてのカスタム情報、送料に関して配送業者を呼び出す方法に関する情報、またはパッケージの返却方法についての情報を追加することもできます。 これらのシナリオを処理するため、受注処理のための梱包明細プロセスの延長ポイントが、バックオフィス、ビジネス ロジック層である Commerce Runtime (CRT)、および POS で追加されました。 これらの拡張ポイントを使用すると、拡張を介してカスタム フローとロジックを追加できます。

## <a name="pos"></a>POS
POS では、**PrintPackingSlipClientRequestHandler** という名前の新しい要求ハンドラーで拡張機能をオーバーライドできます。 この要求は、POS で **梱包明細を印刷する** ボタンを選択すると呼び出されます。 この要求を上書きすることによって、POS でカスタム ロジックを使用することができます。 たとえば、独自の印刷メソッドを呼び出し、追加情報を印刷できます。

たとえば、既定では、PDF 形式で梱包明細を印刷することができます。 POS クライアント要求を上書きすることによって、さまざまな形式で梱包明細を印刷できます。 または、特定の条件を確認し、基本的な条件に基づいて梱包明細の印刷、または印刷停止をすることができます。 また、印刷前に検証を実行して、印刷ロジックまたはカスタム ロジックを止めることができます。 ただし、印刷される実際のデータを変更する場合、CRT およびバックオフィスでビジネス ロジックを変更する必要があります。

### <a name="override-printpackingslipclientrequesthandler"></a>PrintPackingSlipClientRequestHandler のオーバーライド
POS の要求をオーバーライドするには、POS で次のオーバーライド ハンドラー パターンを使用します。

**例**

```typescript
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

要求を上書きした後は、新しい要求ハンドラー情報を含む manifest.json ファイルを更新します。

```typescript 
"requestHandlers": [
    {
        "modulePath": "Handlers/PrintPackingSlipClientRequestHandlerExt"
    }
]
```

## <a name="crt"></a>CRT
POS クライアントの要求ハンドラーと同様、カスタム ロジックの拡張機能を有効にするため CRT に新しい要求が追加されました。

### <a name="markaspickedrealtimerequest"></a>MarkAsPickedRealtimeRequest
**MarkAsPickedRealtimeRequest** 要求は、調達のための明細行をピッキング済みとしてマークします。 明細行がピッキング済みとマークされる前に、カスタム ロジックを追加することができます。 たとえば、プロパティを変更できます。 後で、ピッキング済の明細行の情報が梱包明細の印刷に使用されます。 シナリオに基づいて、この要求を無効にするか、プレトリガーまたはポストトリガーを追加することができます。 

たとえば、 フルフィルメント明細行については、品目の重量などを計算します。 この場合、サービスをカスタマイズできます。 

> [!NOTE]
> バックオフィスでカスタマイズを必要とするロジックを決定する必要がある場合、CRT でカスタマイズするのではなく、バックオフィス レベルでカスタマイズできます。 たとえば、各明細行の品目重量を取得したいが、その情報はバックオフィスでのみ使用できる場合です。 この場合、関連するリアルタイム サービスのメソッドをカスタマイズしてから、バック オフィスから CRT に結果を返すことができます。

### <a name="packfulfillmentlinesrealtimerequest"></a>PackFulfillmentLinesRealtimeRequest
**PackFulfillmentLinesRealtimeRequest** 要求は、フルフィルメント明細行のステータスを **部分的に梱包済み** または **梱包済み** に更新します。 シナリオに基づいて、このサービスを無効にするか、プレトリガーまたはポストトリガーを追加することができます。 

## <a name="headquarters"></a>バックオフィス
バックオフィスでは、梱包明細情報を取得して、拡張機能によってカスタム情報やロジックを追加するために、新しいリアルタイム サービス メソッドが追加されました。 カスタマイズで、データまたはロジックがバックオフィスで実行されることを必須としている場合、拡張機能のパターンを使用して、これらのメソッドをカスタマイズできます。 また、取引サービス クライアント クラスを使用する拡張子シナリオが必要な場合は、CRT からこれらのメソッドを呼び出すことができます。

### <a name="retailtransactionservicefulfillment"></a>RetailTransactionServiceFulfillment
梱包明細プロセスに関連付けられているすべての新しいメソッドは注文のフルフィルメントにより、**RetailTransactionServiceFulfillment** クラスに追加されます。

### <a name="getpackingslipsdata"></a>GetPackingSlipsData
**GetPackingSlipsData** メソッドは、パラメーターとして販売 ID を渡すことによってすべての梱包明細情報を返します。 

### <a name="getfulfillmentlinesbypackingslipid"></a>GetFulfillmentLinesByPackingSlipId
**GetFulfillmentLinesByPackingSlipId** メソッドは、梱包明細 ID に基づいて調達のための明細行を返します。 たとえば、梱包明細 ID があり、その梱包明細 ID に関連する販売明細行を取得する場合、このメソッドを使用します。

### <a name="markfulfillmentlinesaspacked"></a>MarkFulfillmentLinesAsPacked
**MarkFulfillmentLinesAsPacked** メソッドは、調達のための詳細を XML 文字列形式でパラメーターとして取得することにより梱包される調達のための明細行のステータスを更新します。 POS は、POS ユーザー インターフェイス (UI) の選択した明細行をピッキング済としてマークするために CRT を呼び出します。 CRT の **MarkAsPickedRealtimeRequest** 要求がバックオフィスで **MarkFulfillmentLinesAsPacked** リアルタイム サービス メソッドを呼び出し、行のステータスを **梱包済み** として設定します。

行が梱包済みとマークされていて印刷のために返された場合にカスタム ロジックを追加したり追加情報を返すには、**packingSlipExtensionPoint** メソッドをカスタマイズできます。

### <a name="packingslipextensionpoint"></a>packingSlipExtensionPoint
**packingSlipExtensionPoint** メソッドをカスタマイズして、カスタム ロジックを追加、または梱包明細 ID とともにカスタム情報を戻すことができます。 このカスタム情報には、梱包情報または納品書が含まれています。 このメソッドは、通常、カスタム シナリオの拡張機能に追加されます。 このメソッドは、コマンド拡張ポイントのチェーンを使用して **MarkFulfillmentLinesAsPacked** メソッドから呼び出されます。 **MarkFulfillmentLinesAsPacked** メソッドは、CRT コードが行うリアルタイム サービス呼び出しから実行されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]