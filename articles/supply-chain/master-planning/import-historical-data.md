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
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="77819-104">需要予測の履歴データのインポート</span><span class="sxs-lookup"><span data-stu-id="77819-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77819-105">需要予測の精度を確保するには、品目または品目配賦キーごとに、できるだけ多くの履歴需要データを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77819-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="77819-106">履歴需要データがまだインポートされていない場合は、Dynamics 365 Supply Chain Management の **履歴外需** (ReqDemPlanHistoricalExternalDemandEntity) データ エンティティを使用してインポートします。</span><span class="sxs-lookup"><span data-stu-id="77819-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="77819-107">**データ管理** ワークスペースで、エンティティのすべてのフィールドの概要を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="77819-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="77819-108">**データ管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="77819-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="77819-109">**データ エンティティ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="77819-110">エンティティの一覧で、**履歴外需** を探します。</span><span class="sxs-lookup"><span data-stu-id="77819-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="77819-111">**ターゲット フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-111">Select **Target fields**.</span></span> <span data-ttu-id="77819-112">次のエンティティ フィールドは必須です: サイト (**DeliveringSiteId**)、日付 (**DemandDate**)、数量 (**DemandQuantity**)、および品目番号 (**ItemNumber**) か品目配賦キー (**ProductAllocationKeyId**) のいずれか。</span><span class="sxs-lookup"><span data-stu-id="77819-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="77819-113">データ エンティティを使用するには、履歴需要データを含む Microsoft Excel ファイルまたはコンマ区切り値 (CSV) ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="77819-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="77819-114">次の例では、CSV ファイルからデータをインポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="77819-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="77819-115">インポート後のデータのクリーンアップ方法など、データのインポート方法の詳細については、[データのインポートとエクスポートのジョブの概要](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) 、と関連トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77819-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="77819-116">例</span><span class="sxs-lookup"><span data-stu-id="77819-116">Example</span></span>

<span data-ttu-id="77819-117">次のファイルを例として使用できます。</span><span class="sxs-lookup"><span data-stu-id="77819-117">You can use the following file as an example.</span></span> <span data-ttu-id="77819-118">[HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="77819-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="77819-119">このファイルには、品目 D0001 の需要履歴データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="77819-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="77819-120">また、次の必須フィールドのみが含まれています: サイト、数量、および需要の日付。</span><span class="sxs-lookup"><span data-stu-id="77819-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="77819-121">履歴需要データをインポートする会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="77819-122">**データ管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="77819-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="77819-123">**インポート** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="77819-124">インポート プロジェクトの名前を入力します (たとえば、**品目 D0001 の履歴需要のインポート**)。</span><span class="sxs-lookup"><span data-stu-id="77819-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="77819-125">**ソース データ形式** フィールドで、インポートするファイルのファイル形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="77819-126">この例の HistoricalDemandData ファイルをインポートするには、**CSV** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="77819-127">**エンティティ名** フィールドで、**履歴外需** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="77819-128">ファイルをコンピューターに保存して、アップロードします。</span><span class="sxs-lookup"><span data-stu-id="77819-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="77819-129">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77819-129">Select **Import**.</span></span>
9. <span data-ttu-id="77819-130">**実行の要約** ページが自動的に開きます。</span><span class="sxs-lookup"><span data-stu-id="77819-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="77819-131">インポート データをページで確認します。</span><span class="sxs-lookup"><span data-stu-id="77819-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="77819-132">履歴需要データをインポートした後、需要予測を生成できます。</span><span class="sxs-lookup"><span data-stu-id="77819-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77819-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="77819-133">Additional resources</span></span>

[<span data-ttu-id="77819-134">統計ベースライン予測の生成</span><span class="sxs-lookup"><span data-stu-id="77819-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="77819-135">データ インポート/エクスポート ジョブの概要</span><span class="sxs-lookup"><span data-stu-id="77819-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]