---
title: 需要予測の履歴データのインポート
description: 正確な需要予測を取得するには、品目または品目配賦キーごとの履歴需要データが必要です。 このトピックでは、需要予測データの長期的な履歴が残るよう、任意のシステムから履歴需要データをインポートするためにデータ エンティティを使用する方法について説明します。
author: ChristianRytt
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6dba31279541c20949dd1e86236103045c48b701
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579667"
---
# <a name="import-historical-data-for-demand-forecasts"></a>需要予測の履歴データのインポート

[!include [banner](../includes/banner.md)]

需要予測の精度を確保するには、品目または品目配賦キーごとに、できるだけ多くの履歴需要データを取得する必要があります。 履歴需要データがまだインポートされていない場合は、Dynamics 365 Supply Chain Management の **履歴外需** (ReqDemPlanHistoricalExternalDemandEntity) データ エンティティを使用してインポートします。

**データ管理** ワークスペースで、エンティティのすべてのフィールドの概要を表示することができます。

1. **データ管理** ワークスペースを開きます。
2. **データ エンティティ** タイルを選択します。
3. エンティティの一覧で、**履歴外需** を探します。
4. **ターゲット フィールド** を選択します。 次のエンティティ フィールドは必須です: サイト (**DeliveringSiteId**)、日付 (**DemandDate**)、数量 (**DemandQuantity**)、および品目番号 (**ItemNumber**) か品目配賦キー (**ProductAllocationKeyId**) のいずれか。

データ エンティティを使用するには、履歴需要データを含む Microsoft Excel ファイルまたはコンマ区切り値 (CSV) ファイルが必要です。 次の例では、CSV ファイルからデータをインポートする方法を示します。

インポート後のデータのクリーンアップ方法など、データのインポート方法の詳細については、[データのインポートとエクスポートのジョブの概要](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) 、と関連トピックを参照してください。

[統計ベースライン予測を生成する](generate-statistical-baseline-forecast.md)も参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]