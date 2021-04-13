---
title: データベース移動操作 - 調整
description: このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) の調整の概要について説明します。
author: laneswenka
ms.date: 02/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 530a80bb0f8012c2bae9792a420e23da45b97908
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752774"
---
# <a name="throttling"></a><span data-ttu-id="8ef76-103">調整</span><span class="sxs-lookup"><span data-stu-id="8ef76-103">Throttling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ef76-104">このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) の調整の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ef76-104">This topic provides an overview of throttling for the Database Movement application programming interface (API).</span></span>

## <a name="rate-limits"></a><span data-ttu-id="8ef76-105">レート制限</span><span class="sxs-lookup"><span data-stu-id="8ef76-105">Rate limits</span></span>

<span data-ttu-id="8ef76-106">サービスの信頼性を維持し、コストを削減するために、データベース移動 API に対する調整が有効になります。</span><span class="sxs-lookup"><span data-stu-id="8ef76-106">To help maintain the reliability of the service and reduce costs, throttling will be turned on for the Database Movement API.</span></span> <span data-ttu-id="8ef76-107">調整は、RESTful エンドポイントが悪用されたり、過度に使用されたりするのを防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8ef76-107">Throttling helps protect against malicious and excessive use of the RESTful endpoints.</span></span> <span data-ttu-id="8ef76-108">データベース移動操作は、Microsoft Dynamics Lifecycle Services (LCS) から実行できる最も時間がかかるおよび CPU に非常に負荷がかかるタスクの一部であり、Microsoft は現在の呼び出し制限を後で変更する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8ef76-108">Database movement operations are some of the most time-consuming and CPU-intensive tasks that can be run from Microsoft Dynamics Lifecycle Services (LCS), and Microsoft might change the current call limits later.</span></span>

### <a name="current-limits"></a><span data-ttu-id="8ef76-109">現在の制限</span><span class="sxs-lookup"><span data-stu-id="8ef76-109">Current limits</span></span>

<span data-ttu-id="8ef76-110">現在、データベース移動 API では、LCS での新しい操作をトリガーするすべてのアクションに対して、**24 時間枠あたり 3 回の実行** というグローバルな呼び出し制限があります。</span><span class="sxs-lookup"><span data-stu-id="8ef76-110">Currently, the Database Movement API has a global call limit of **three executions per 24-hour timeframe** for all actions that trigger a new operation in LCS.</span></span> <span data-ttu-id="8ef76-111">これらの操作には、データベースの更新操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ef76-111">These operations include database refresh operations.</span></span>

<span data-ttu-id="8ef76-112">この制限を超えた場合は、新しい操作を開始することはできず、次の例のようなエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ef76-112">If you exceed the limit, you won't be able to start a new operation and will receive an error that resembles the following example.</span></span>

```json
{
    "IsSuccess": false,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": "Maximum allowed API operations are 3 from 2019-09-30T04:01:01.9999999",
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]