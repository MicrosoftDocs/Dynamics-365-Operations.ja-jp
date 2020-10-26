---
title: 需要予測の履歴データのインポート
description: 正確な需要予測を取得するには、品目または品目配賦キーごとの履歴需要データが必要です。 このトピックでは、需要予測データの長期的な履歴が残るよう、任意のシステムから履歴需要データをインポートするためにデータ エンティティを使用する方法について説明します。
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66481b1dd8650960cad2947425c1e6c7450afcb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982824"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="ba359-104">需要予測の履歴データのインポート</span><span class="sxs-lookup"><span data-stu-id="ba359-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba359-105">需要予測の精度を確保するには、品目または品目配賦キーごとに、できるだけ多くの履歴需要データを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba359-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="ba359-106">履歴需要データがまだインポートされていない場合は、Dynamics 365 Supply Chain Management の**履歴外需** (ReqDemPlanHistoricalExternalDemandEntity) データ エンティティを使用してインポートします。</span><span class="sxs-lookup"><span data-stu-id="ba359-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="ba359-107">**データ管理**ワークスペースで、エンティティのすべてのフィールドの概要を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="ba359-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="ba359-108">**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="ba359-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="ba359-109">**データ エンティティ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ba359-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="ba359-110">エンティティの一覧で、**履歴外需**を探します。</span><span class="sxs-lookup"><span data-stu-id="ba359-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="ba359-111">**ターゲット フィールド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ba359-111">Click **Target fields**.</span></span> <span data-ttu-id="ba359-112">次のエンティティ フィールドは必須です: サイト (**DeliveringSiteId**)、日付 (**DemandDate**)、数量 (**DemandQuantity**)、および品目番号 (**ItemNumber**) か品目配賦キー (**ProductAllocationKeyId**) のいずれか。</span><span class="sxs-lookup"><span data-stu-id="ba359-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="ba359-113">データ エンティティを使用するには、履歴需要データを含む Microsoft Excel ファイルまたはコンマ区切り値 (CSV) ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="ba359-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="ba359-114">次の例では、CSV ファイルからデータをインポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ba359-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="ba359-115">例</span><span class="sxs-lookup"><span data-stu-id="ba359-115">Example</span></span>

<span data-ttu-id="ba359-116">次のファイルを例として使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba359-116">You can use the following file as an example.</span></span> <span data-ttu-id="ba359-117">[HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="ba359-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="ba359-118">このファイルには、品目 D0001 の需要履歴データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba359-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="ba359-119">また、次の必須フィールドのみが含まれています: サイト、数量、および需要の日付。</span><span class="sxs-lookup"><span data-stu-id="ba359-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="ba359-120">履歴需要データをインポートする会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba359-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="ba359-121">**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="ba359-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="ba359-122">**インポート** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ba359-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="ba359-123">インポート プロジェクトの名前を入力します (たとえば、**品目 D0001 の履歴需要のインポート**)。</span><span class="sxs-lookup"><span data-stu-id="ba359-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="ba359-124">**ソース データ形式** フィールドで、インポートするファイルのファイル形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba359-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="ba359-125">この例の HistoricalDemandData ファイルをインポートするには、**CSV** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba359-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="ba359-126">**エンティティ名** フィールドで、**履歴外需** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba359-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="ba359-127">ファイルをコンピューターに保存して、アップロードします。</span><span class="sxs-lookup"><span data-stu-id="ba359-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="ba359-128">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ba359-128">Click **Import**.</span></span>
9. <span data-ttu-id="ba359-129">**実行の要約** ページが自動的に開きます。</span><span class="sxs-lookup"><span data-stu-id="ba359-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="ba359-130">インポート データをページで確認します。</span><span class="sxs-lookup"><span data-stu-id="ba359-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="ba359-131">履歴需要データをインポートした後、需要予測を生成できます。</span><span class="sxs-lookup"><span data-stu-id="ba359-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba359-132">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="ba359-132">Additional resources</span></span>

[<span data-ttu-id="ba359-133">統計ベースライン予測の生成</span><span class="sxs-lookup"><span data-stu-id="ba359-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
