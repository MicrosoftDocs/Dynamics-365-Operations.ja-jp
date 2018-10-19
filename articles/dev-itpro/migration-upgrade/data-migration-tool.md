---
title: "AX 2009 アップグレード - Dynamics AX 2009 から Dynamics 365 for Finance and Operations に移行するデーの移行ツールを使用する"
description: "このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行するために、データ移行ツール (DMT) を使用する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: c69143953d77d25de7eda971875b4ff9a81addb0
ms.contentlocale: ja-jp
ms.lasthandoff: 09/20/2018

---

# <a name="ax-2009-upgrade---use-the-data-migration-tool-to-migrate-from-dynamics-ax-2009-to-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="e83ad-103">AX 2009 アップグレード - Dynamics AX 2009 から Dynamics 365 for Finance and Operations に移行するデーの移行ツールを使用する</span><span class="sxs-lookup"><span data-stu-id="e83ad-103">AX 2009 upgrade - Use the Data migration tool to migrate from Dynamics AX 2009 to Dynamics 365 for Finance and Operations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e83ad-104">AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行するために、Microsoft Dynamics AX 2009 データ移行ツール (DMT) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e83ad-104">You can use the Microsoft Dynamics AX 2009 Data migration tool (DMT) to migrate your data from AX 2009 to Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e83ad-105">DMT の使用は、AX 2009 から Finance and Operations へのアップグレード パスでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e83ad-105">Using the DMT is the only supported upgrade path from AX 2009 to Finance and Operations.</span></span> <span data-ttu-id="e83ad-106">DMT では、AX 2009 と Finance and Operations のテーブル スキーマを検索してその間のギャップを埋めることができるだけでなく、データを移動できます。</span><span class="sxs-lookup"><span data-stu-id="e83ad-106">The DMT helps you find and fill gaps between the table schemas of AX 2009 and Finance and Operations, as well as helping you move your data.</span></span> 

## <a name="archictecture"></a><span data-ttu-id="e83ad-107">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="e83ad-107">Archictecture</span></span>
<span data-ttu-id="e83ad-108">次の図では、DMT のアーキテクチャ、ソース システム (AX 2009) のデータの処理方法とターゲット システム (Finance and Operations) に移動する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-108">The following illustration describes the architecture of the DMT, and how data from the source system (AX 2009) is processed and moved to the target system (Finance and Operations).</span></span>

![データ移行の技術フロー](media/dmt_technical_flow.png)

## <a name="data-migration-process"></a><span data-ttu-id="e83ad-110">データ移行プロセス</span><span class="sxs-lookup"><span data-stu-id="e83ad-110">Data migration process</span></span>

<span data-ttu-id="e83ad-111">次の図では、AX 2009 インスタンスでデータを収集して準備し、Finance and Operations 環境にそのデータをインポートする全体的なプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-111">The following illustration shows the overall process of collecting and preparing the data in your AX 2009 instance and then importing that data into your Finance and Operations environment.</span></span>

![データ移行プロセス](media/dmt_process_flow.PNG)

<span data-ttu-id="e83ad-113">DMT を使用してソース環境 (AX 2009) からデータをエクスポートするには、次の処理前の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e83ad-113">Before you can use the DMT to export data from the source environment (AX 2009), you must complete the following pre-processing tasks:</span></span>

- <span data-ttu-id="e83ad-114">ソース環境とターゲット環境との間のテーブル フィールドのマッピング</span><span class="sxs-lookup"><span data-stu-id="e83ad-114">Mapping the table fields between the source and target environments</span></span>
- <span data-ttu-id="e83ad-115">ソース データへの変換の適用</span><span class="sxs-lookup"><span data-stu-id="e83ad-115">Applying conversions to the source data</span></span>
- <span data-ttu-id="e83ad-116">ソース データの既定値の設定</span><span class="sxs-lookup"><span data-stu-id="e83ad-116">Setting up default values for the source data</span></span>
- <span data-ttu-id="e83ad-117">クエリ フィルターの適用</span><span class="sxs-lookup"><span data-stu-id="e83ad-117">Applying query filters</span></span>

<span data-ttu-id="e83ad-118">ソース システムには複数の法人が存在することがあるため、移行するデータを含む法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e83ad-118">Because there can be multiple legal entities in the source system, you must select the legal entities that contain the data to migrate.</span></span> <span data-ttu-id="e83ad-119">選択した法人について、ソース テーブルとその行カウントを確認します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-119">For the selected legal entities, you can review the source tables and their row counts.</span></span> <span data-ttu-id="e83ad-120">仮想会社を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="e83ad-120">You can also view any virtual companies.</span></span> <span data-ttu-id="e83ad-121">最後に、法人が関連付けられている仮想会社と関連するテーブルを分析できます。</span><span class="sxs-lookup"><span data-stu-id="e83ad-121">Finally, you can analyze virtual companies that legal entities are attached to and the related tables.</span></span>

<span data-ttu-id="e83ad-122">エクスポートしたデータの移行を成功させるには、ソース テーブルが同等のターゲット データ エンティティにマップされていることが必要です。</span><span class="sxs-lookup"><span data-stu-id="e83ad-122">Successful migration of exported data requires that a source table be mapped to an equivalent target data entity.</span></span> <span data-ttu-id="e83ad-123">マッピングを設定するには、各テーブルのソース フィールドとターゲット フィールドの自動マッピングを可能にする Microsoft Excel マッピング ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-123">You set up the mapping by using a Microsoft Excel mapping file that allows for automatic mapping of the source and target fields of each table.</span></span> <span data-ttu-id="e83ad-124">マッピング ファイルには、データ エンティティの Finance and Operations スキーマからのデータと、いくつかのテーブルで必要な既定のデータも含まれます。</span><span class="sxs-lookup"><span data-stu-id="e83ad-124">The mapping file also includes the data from the Finance and Operations schema of the data entities and the default data that is required in some tables.</span></span>

<span data-ttu-id="e83ad-125">AX 2009 から Finance and Operations にデータを移行する前に、移行の要件を満たすために次の作業を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e83ad-125">Before you can migrate data from AX 2009 to Finance and Operations, you must complete the following tasks to meet the migration requirements:</span></span>

- <span data-ttu-id="e83ad-126">選択した法人に基づいてに入力されたソース分析コードに対応する目標の分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-126">Select target dimensions that correspond to the source dimensions that are populated based on the selected legal entities.</span></span>
- <span data-ttu-id="e83ad-127">選択した法人に含まれている在庫分析コードを確認します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-127">Review the inventory dimensions that are included with the selected legal entities.</span></span>
- <span data-ttu-id="e83ad-128">各法人の勘定科目表を選択するか、単一の勘定科目に複数の法人を連結します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-128">Select the chart of accounts for each legal entity, or consolidate multiple legal entities into a single chart of accounts.</span></span>
- <span data-ttu-id="e83ad-129">基本的な元帳設定を実行します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-129">Complete the basic ledger setup.</span></span>
- <span data-ttu-id="e83ad-130">フィールドの拡張データ型 (EDT) に基づき、ソース データにデータ変換を適用します。</span><span class="sxs-lookup"><span data-stu-id="e83ad-130">Apply data conversions to the source data, based on the extended data type (EDT) of the field.</span></span>

