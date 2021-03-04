---
title: 標準データ エンティティに関する情報を検索します。
description: このトピックでは、使用可能な標準データ エンティティに関する情報を取得する方法、およびレポートを実行するスクリプトをダウンロードする方法について説明します。
author: robinarh
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 202654
ms.assetid: 6ec8ea87-ea1e-4a10-9d67-2b6565c5c62e
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 387179b0d422ae9108e7af03963a696db54796bb
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154101"
---
# <a name="find-information-about-standard-data-entities"></a><span data-ttu-id="36357-103">標準データ エンティティに関する情報の検索</span><span class="sxs-lookup"><span data-stu-id="36357-103">Find information about standard data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36357-104">アプリケーションには、既定のデータ エンティティが数多く含まれています。</span><span class="sxs-lookup"><span data-stu-id="36357-104">The application ships with many default data entities.</span></span> <span data-ttu-id="36357-105">データ エンティティは頻繁に更新されるため、ドキュメント化のために、データ エンティティ テンプレートを使用して、どのオーダーデータエンティティをインポートする必要があるかを示します。また、各リリースで出荷されるデータ エンティティのリストも使用します。</span><span class="sxs-lookup"><span data-stu-id="36357-105">Data entities are frequently updated, so for documentation, we rely on the data entity templates to indicate which order data entities should be imported in, and on reports for a list of data entities that ship with each release.</span></span>

## <a name="configuration-data-packages"></a><span data-ttu-id="36357-106">コンフィギュレーション データ パッケージ</span><span class="sxs-lookup"><span data-stu-id="36357-106">Configuration data packages</span></span>

<span data-ttu-id="36357-107">Microsoft Dynamics Lifecycle Services (LCS) のコンフィギュレーション データ パッケージには、コンフィギュレーション エンティティのスプレッドシートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="36357-107">Configuration data packages on Microsoft Dynamics Lifecycle Services (LCS) contain configuration entity spreadsheets.</span></span> <span data-ttu-id="36357-108">コンフィギュレーション エンティティ スプレッドシートには、実装の初期ゴールド ビルドを作成するために使用できるベスト プラクティス データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="36357-108">Configuration entity spreadsheets contain best practice data that you can use to create an initial golden build of an implementation.</span></span> <span data-ttu-id="36357-109">XML ファイルを使用してデータ パッケージ内のデータ エンティティも適切に順序付けされ、1 回のクリックによるインポートを成功させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="36357-109">The data entities in the data packages are also sequenced appropriately using an XML file to help guarantee a successful single-click import of the data.</span></span> <span data-ttu-id="36357-110">データのインポートを指示することをどうしてお勧めしているかを理解していただくために、コンフィギュレーション データ パッケージをダウンロードして確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="36357-110">We recommend that you download and review the configuration data packages to understand how we recommend that you order your data imports.</span></span> <span data-ttu-id="36357-111">詳細については、 [データ テンプレートの構成](configuration-data-templates.md) および [会社間、または法人間で構成データをコピーする](copy-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36357-111">For more information, see [Configuration data templates](configuration-data-templates.md) and [Copy configuration data between companies or legal entities overview](copy-configuration.md).</span></span>

## <a name="reports"></a><span data-ttu-id="36357-112">レポート</span><span class="sxs-lookup"><span data-stu-id="36357-112">Reports</span></span>

<span data-ttu-id="36357-113">Microsoft は、データ エンティティの次のレポートを提供しており、[技術参照レポート](https://docs.microsoft.com/dynamics/s-e/)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="36357-113">Microsoft provides the following reports for data entities, which can be downloaded from [Technical reference reports](https://docs.microsoft.com/dynamics/s-e/):</span></span>

- <span data-ttu-id="36357-114">データ エンティティの集計: 集計するデータ エンティティと、それぞれに含まれるフィールドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-114">Aggregate data entities: Lists the aggregate data entities, and the fields that each contains.</span></span>
- <span data-ttu-id="36357-115">メジャーの集計: 集計するメジャーを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-115">Aggregate measures: Lists the aggregate measures.</span></span>
- <span data-ttu-id="36357-116">コンフィギュレーション キー: コンフィギュレーション キーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36357-116">Config keys: Lists the configuration keys.</span></span> 
- <span data-ttu-id="36357-117">コンフィギュレーション キー グループ: コンフィギュレーション キー グループの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36357-117">Config key groups: Lists the configuration key groups.</span></span>
- <span data-ttu-id="36357-118">データ エンティティ: 各データ エンティティを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-118">Data entities: Lists each data entity.</span></span> <span data-ttu-id="36357-119">レポートには、エンティティのデータ ソースとエンティティに含まれるフィールドが示されます。</span><span class="sxs-lookup"><span data-stu-id="36357-119">The report indicates the data source of the entity and the fields included in the entity.</span></span> <span data-ttu-id="36357-120">このレポートは、データ エンティティが公開されているかどうかも示します。</span><span class="sxs-lookup"><span data-stu-id="36357-120">The report also indicates whether the data entity is public.</span></span>
- <span data-ttu-id="36357-121">データ エンティティ フィールド: データ エンティティの各フィールドと、その元になったテーブルを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-121">Data entities fields: Lists each field in a data entity, and the table that it originates from.</span></span>
- <span data-ttu-id="36357-122">KPI: KPI を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-122">KPIs: Lists the KPIs.</span></span>
- <span data-ttu-id="36357-123">ライセンス コード: 各コンフィギュレーション キーに関連付けられているライセンス コードの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-123">License codes: Lists the license code associated with each configuration key.</span></span>
- <span data-ttu-id="36357-124">メニュー項目: 各コンフィギュレーション キーに関連付けられているメニュー項目を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-124">Menu items: Lists the menu items associated with each configuration key.</span></span>
- <span data-ttu-id="36357-125">SSRS レポート: 各レポートを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-125">SSRS reports: Lists each report.</span></span> <span data-ttu-id="36357-126">レポートには、各レポートで使用されるデータ セットと、各レポートで使用可能なフィルターおよびフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36357-126">The report indicates the data set used for each report, as well as the filters and fields available on each report.</span></span>
- <span data-ttu-id="36357-127">テーブル: 各テーブルとそのテーブル グループの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-127">Tables: Lists each table and its table group.</span></span>
- <span data-ttu-id="36357-128">ワークフロー タイプ: 各種のワークフローを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="36357-128">Workflow type: Lists each type of workflow.</span></span> <span data-ttu-id="36357-129">レポートでは、ワークフローの各タイプの使用目的を説明し、各タイプのワークフローが組織内の特定の法人または組織全体に関連付けられているかどうかも示されます。</span><span class="sxs-lookup"><span data-stu-id="36357-129">The report also describes what each type of workflow is used for and indicates whether the workflows of each type are associated with a specific company in the organization or with the whole organization.</span></span>

## <a name="scripts"></a><span data-ttu-id="36357-130">スクリプト</span><span class="sxs-lookup"><span data-stu-id="36357-130">Scripts</span></span>

<span data-ttu-id="36357-131">これらのレポートを実行するスクリプトを、[fin-ops-doc-scripts](https://github.com/microsoft/fin-ops-doc-scripts) からダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="36357-131">You can download the scripts to run these reports from [fin-ops-doc-scripts](https://github.com/microsoft/fin-ops-doc-scripts).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36357-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="36357-132">Additional resources</span></span>

[<span data-ttu-id="36357-133">データ エンティティの概要</span><span class="sxs-lookup"><span data-stu-id="36357-133">Data entities overview</span></span>](data-entities.md)
