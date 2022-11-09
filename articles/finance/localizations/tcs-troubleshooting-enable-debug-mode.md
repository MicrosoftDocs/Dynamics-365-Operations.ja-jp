---
title: 税計算サービスでデバッグ モードを有効化する
description: この記事では、税計算サービスにおいてデバッグ モードを有効にし、問題に対処する方法について説明します。
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2bb381939ebe32cb51caf730cdd441557d83a4c0
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2022
ms.locfileid: "9620901"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>税計算サービスでデバッグ モードを有効化する

[!include [banner](../includes/banner.md)]

この記事では、税計算サービスにおいてデバッグ モードを有効にし、問題に対処する方法について説明します。

1. Application Object Server (AOS) の URL に、**&debug=vs%2CconfirmExit&** を追加し、ページを最新の情報に更新します。
2. 消費税を計算するために **消費税** を選択した場合、**TaxServiceTroubleshootingLog.txt** という名前のテキスト ファイルが開きます。 **TaxServiceTroubleshootingLog.txt** ファイルには、**TaxableDocument** と計算パラメーターが含まれます。 これらの結果は、税サービスおよびトラブルシューティングの例外情報により返されます。

## <a name="sample"></a>サンプル

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
