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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301653"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="36fb6-104">需要予測の履歴データのインポート</span><span class="sxs-lookup"><span data-stu-id="36fb6-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36fb6-105">需要予測の精度を確保するには、品目または品目配賦キーごとに、できるだけ多くの履歴需要データを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36fb6-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="36fb6-106">履歴需要データがまだインポートされていない場合は、Dynamics 365 Supply Chain Management の **履歴外需** (ReqDemPlanHistoricalExternalDemandEntity) データ エンティティを使用してインポートします。</span><span class="sxs-lookup"><span data-stu-id="36fb6-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="36fb6-107">**データ管理** ワークスペースで、エンティティのすべてのフィールドの概要を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="36fb6-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="36fb6-108">**データ管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="36fb6-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="36fb6-109">**データ エンティティ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="36fb6-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="36fb6-110">エンティティの一覧で、**履歴外需** を探します。</span><span class="sxs-lookup"><span data-stu-id="36fb6-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="36fb6-111">**ターゲット フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fb6-111">Select **Target fields**.</span></span> <span data-ttu-id="36fb6-112">次のエンティティ フィールドは必須です: サイト (**DeliveringSiteId**)、日付 (**DemandDate**)、数量 (**DemandQuantity**)、および品目番号 (**ItemNumber**) か品目配賦キー (**ProductAllocationKeyId**) のいずれか。</span><span class="sxs-lookup"><span data-stu-id="36fb6-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="36fb6-113">データ エンティティを使用するには、履歴需要データを含む Microsoft Excel ファイルまたはコンマ区切り値 (CSV) ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="36fb6-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="36fb6-114">次の例では、CSV ファイルからデータをインポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="36fb6-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="36fb6-115">インポート後のデータのクリーンアップ方法など、データのインポート方法の詳細については、[データのインポートとエクスポートのジョブの概要](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) 、と関連トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="36fb6-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="36fb6-116">[統計ベースライン予測を生成する](generate-statistical-baseline-forecast.md)も参照してください。</span><span class="sxs-lookup"><span data-stu-id="36fb6-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]