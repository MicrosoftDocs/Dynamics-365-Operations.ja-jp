---
title: "需要予測の履歴データのインポート"
description: "正確な需要予測を取得するには、品目または品目配賦キーごとの履歴需要データが必要です。 このトピックでは、需要予測データの長期的な履歴が残るよう、任意のシステムから履歴需要データをインポートするためにデータ エンティティを使用する方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>需要予測の履歴データのインポート

[!include[banner](../includes/banner.md)]

需要予測の精度を確保するには、品目または品目配賦キーごとに、できるだけ多くの履歴需要データを取得する必要があります。 履歴需要データがまだインポートされていない場合は、Microsoft Dynamics 365 for Operations の**履歴外需** (ReqDemPlanHistoricalExternalDemandEntity) データ エンティティを使用してインポートします。

**データ管理**ワークスペースで、エンティティのすべてのフィールドの概要を表示することができます。

1. **データ管理**ワークスペースを開きます。
2. [**データ エンティティ**] タイルをクリックします。
3. エンティティの一覧で、**履歴外需**を探します。
4. [**ターゲット フィールド**] をクリックします。 次のエンティティ フィールドは必須です: サイト (**DeliveringSiteId**)、日付 (**DemandDate**)、数量 (**DemandQuantity**)、および品目番号 (**ItemNumber**) か品目配賦キー (**ProductAllocationKeyId**) のいずれか。

データ エンティティを使用するには、過去の需要データを含む Microsoft Excel ファイルまたはコンマ区切り値 (CSV) ファイルが必要です。 次の例では、CSV ファイルからデータをインポートする方法を示します。

## <a name="example"></a>例

次のファイルを例として使用できます。 [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) をダウンロードします。 このファイルには、品目 D0001 の需要履歴データが含まれています。 また、次の必須フィールドのみが含まれています: サイト、数量、および需要の日付。

1. 履歴需要データをインポートする会社を選択します。
2. **データ管理**ワークスペースを開きます。
3. [**インポート**] タイルをクリックします。
4. インポート プロジェクトの名前を入力します (たとえば、**品目 D0001 の履歴需要のインポート**)。
5. [**ソース データ形式**] フィールドで、インポートするファイルのファイル形式を選択します。 この例の HistoricalDemandData ファイルをインポートするには、[**CSV**] を選択します。
6. [**エンティティ名**] フィールドで、[**履歴外需**] を選択します。
7. ファイルをコンピューターに保存して、アップロードします。
8. [**インポート**] をクリックします。
9. [**実行の要約**] ページが自動的に開きます。 インポート データをページで確認します。

履歴需要データをインポートした後、需要予測を生成できます。

## <a name="see-also"></a>参照

[統計ベースライン予測の生成](generate-statistical-baseline-forecast.md)

