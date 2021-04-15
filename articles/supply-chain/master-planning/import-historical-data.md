---
title: 需要予測の履歴データのインポート
description: 正確な需要予測を取得するには、品目または品目配賦キーごとの履歴需要データが必要です。 このトピックでは、需要予測データの長期的な履歴が残るよう、任意のシステムから履歴需要データをインポートするためにデータ エンティティを使用する方法について説明します。
author: roxanadiaconu
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
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bb3c178a698bdcd46e7c596247360ba9233b398
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816487"
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

## <a name="example"></a>例

次のファイルを例として使用できます。 [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/) をダウンロードします。 このファイルには、品目 D0001 の需要履歴データが含まれています。 また、次の必須フィールドのみが含まれています: サイト、数量、および需要の日付。

1. 履歴需要データをインポートする会社を選択します。
2. **データ管理** ワークスペースを開きます。
3. **インポート** タイルを選択します。
4. インポート プロジェクトの名前を入力します (たとえば、**品目 D0001 の履歴需要のインポート**)。
5. **ソース データ形式** フィールドで、インポートするファイルのファイル形式を選択します。 この例の HistoricalDemandData ファイルをインポートするには、**CSV** を選択します。
6. **エンティティ名** フィールドで、**履歴外需** を選択します。
7. ファイルをコンピューターに保存して、アップロードします。
8. **インポート** を選択します。
9. **実行の要約** ページが自動的に開きます。 インポート データをページで確認します。

履歴需要データをインポートした後、需要予測を生成できます。

## <a name="additional-resources"></a>追加リソース

[統計ベースライン予測の生成](generate-statistical-baseline-forecast.md)  
[データ インポート/エクスポート ジョブの概要](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]