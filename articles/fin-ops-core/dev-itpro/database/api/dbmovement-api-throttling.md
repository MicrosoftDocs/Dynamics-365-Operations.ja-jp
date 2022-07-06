---
title: データベース移動操作 - 調整
description: この記事では、データベース移動アプリケーション プログラミング インターフェイス (API) の調整の概要について説明します。
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
ms.openlocfilehash: fdc082d495ccab1a6b9ccb2442828abec6986d94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867587"
---
# <a name="throttling"></a>調整

[!include [banner](../../includes/banner.md)]

この記事では、データベース移動アプリケーション プログラミング インターフェイス (API) の調整の概要について説明します。

## <a name="rate-limits"></a>レート制限

サービスの信頼性を維持し、コストを削減するために、データベース移動 API に対する調整が有効になります。 調整は、RESTful エンドポイントが悪用されたり、過度に使用されたりするのを防ぐのに役立ちます。 データベース移動操作は、Microsoft Dynamics Lifecycle Services (LCS) から実行できる最も時間がかかるおよび CPU に非常に負荷がかかるタスクの一部であり、Microsoft は現在の呼び出し制限を後で変更する可能性があります。

### <a name="current-limits"></a>現在の制限

現在、データベース移動 API では、LCS での新しい操作をトリガーするすべてのアクションに対して、**24 時間枠あたり 3 回の実行** というグローバルな呼び出し制限があります。 これらの操作には、データベースの更新操作が含まれます。

この制限を超えた場合は、新しい操作を開始することはできず、次の例のようなエラーが表示されます。

```json
{
    "IsSuccess": false,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": "Maximum allowed API operations are 3 from 2019-09-30T04:01:01.9999999",
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]