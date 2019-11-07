---
title: データベース移動操作 - 調整
description: このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) の調整の概要について説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 8512f0cc8e1691d413f7855462bfe521fca5597a
ms.sourcegitcommit: d800613020d5548d100c8f240fb81bb6258a3646
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2019
ms.locfileid: "2573563"
---
# <a name="throttling"></a>調整

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) の調整の概要について説明します。

## <a name="rate-limits"></a>レート制限

サービスの信頼性を維持し、コストを削減するために、データベース移動 API に対する調整が有効になります。 調整は、RESTful エンドポイントが悪用されたり、過度に使用されたりするのを防ぐのに役立ちます。 データベース移動操作は、Microsoft Dynamics Lifecycle Services (LCS) から実行できる最も時間がかかるおよび CPU に非常に負荷がかかるタスクの一部であり、Microsoft は現在の呼び出し制限を後で変更する可能性があります。

### <a name="current-limits"></a>現在の制限

現在、データベース移動 API では、LCS での新しい操作をトリガーするすべてのアクションに対して、**24 時間枠あたり 3 回の実行**というグローバルな呼び出し制限があります。 これらの操作には、データベースの更新操作が含まれます。

この制限を超えた場合は、新しい操作を開始することはできず、次の例のようなエラーが表示されます。

```json
{
    "IsSuccess": false,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": "Maximum allowed API operations are 3 from 2019-09-30T04:01:01.9999999",
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```
