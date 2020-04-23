---
title: AX 2009 アップグレード - データ移行ツールを使用して、Dynamics AX 2009から Dynamics 365 for Finance and Operations へ移行します。
description: このトピックでは、データ移行ツール (DMT) を使用して、 Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行する方法を説明します。
author: kfend
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 1df9cb83e0bdf0a8e2163e562fe30490da8c94f2
ms.sourcegitcommit: 8f5d62d20028484a62304483133c564689b193e3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254295"
---
# <a name="ax-2009-upgrade---use-the-data-migration-tool-to-migrate-from-dynamics-ax-2009-to-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="3a28f-103">AX 2009 アップグレード - データ移行ツールを使用して、Dynamics AX 2009から Dynamics 365 for Finance and Operations へ移行します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-103">AX 2009 upgrade - Use the Data migration tool to migrate from Dynamics AX 2009 to Dynamics 365 for Finance and Operations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a28f-104">AX 2009 から Finance and Operations へデータを移行するため Microsoft Dynamics AX 2009 データ移行ツール (DMT) を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3a28f-104">You can use the Microsoft Dynamics AX 2009 Data migration tool (DMT) to migrate your data from AX 2009 to Finance and Operations.</span></span> <span data-ttu-id="3a28f-105">DMT の使用は、唯一サポートされている AX 2009 からのアップグレード パスです。</span><span class="sxs-lookup"><span data-stu-id="3a28f-105">Using the DMT is the only supported upgrade path from AX 2009.</span></span> <span data-ttu-id="3a28f-106">DMT は、各バージョンのテーブル スキーマ間を検索してその間のギャップを埋めることができ、またデータを移動も行います。</span><span class="sxs-lookup"><span data-stu-id="3a28f-106">The DMT helps you find and fill gaps between the table schemas for each version, as well as helping you move your data.</span></span> 

## <a name="architecture"></a><span data-ttu-id="3a28f-107">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="3a28f-107">Architecture</span></span>
<span data-ttu-id="3a28f-108">次の図では、DMT のアーキテクチャ、また、ソース システム (AX 2009) のデータの処理方法とターゲット システム (Finance and Operations) への移動方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-108">The following illustration describes the architecture of the DMT, and how data from the source system (AX 2009) is processed and moved to the target system (Finance and Operations).</span></span>

![データ移行の技術フロー](media/dmt_technical_flow.png)

## <a name="data-migration-process"></a><span data-ttu-id="3a28f-110">データ移行プロセス</span><span class="sxs-lookup"><span data-stu-id="3a28f-110">Data migration process</span></span>

<span data-ttu-id="3a28f-111">次の図で、AX 2009 インスタンスでデータを収集して準備し、新しい環境にそのデータをインポートする全体的なプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-111">The following illustration shows the overall process of collecting and preparing the data in your AX 2009 instance and then importing that data into your new environment.</span></span>

![データ移行プロセス](media/dmt_process_flow.PNG)

<span data-ttu-id="3a28f-113">DMT を使用してソース環境 (AX 2009) からデータをエクスポートする前に、次の前処理のタスクを完了させておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a28f-113">Before you can use the DMT to export data from the source environment (AX 2009), you must complete the following pre-processing tasks:</span></span>

- <span data-ttu-id="3a28f-114">ソース環境とターゲット環境との間のテーブル フィールドのマッピング</span><span class="sxs-lookup"><span data-stu-id="3a28f-114">Mapping the table fields between the source and target environments</span></span>
- <span data-ttu-id="3a28f-115">ソース データへの変換の適用</span><span class="sxs-lookup"><span data-stu-id="3a28f-115">Applying conversions to the source data</span></span>
- <span data-ttu-id="3a28f-116">ソース データの既定値の設定</span><span class="sxs-lookup"><span data-stu-id="3a28f-116">Setting up default values for the source data</span></span>
- <span data-ttu-id="3a28f-117">クエリ フィルターの適用</span><span class="sxs-lookup"><span data-stu-id="3a28f-117">Applying query filters</span></span>

<span data-ttu-id="3a28f-118">ソース システムには複数の法人が存在することがあるため、移行するデータを含む法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a28f-118">Because there can be multiple legal entities in the source system, you must select the legal entities that contain the data to migrate.</span></span> <span data-ttu-id="3a28f-119">選択した法人について、ソース テーブルとその行カウントを確認します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-119">For the selected legal entities, you can review the source tables and their row counts.</span></span> <span data-ttu-id="3a28f-120">仮想会社を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="3a28f-120">You can also view any virtual companies.</span></span> <span data-ttu-id="3a28f-121">最後に、法人が関連付けられている仮想会社と関連するテーブルを分析できます。</span><span class="sxs-lookup"><span data-stu-id="3a28f-121">Finally, you can analyze virtual companies that legal entities are attached to and the related tables.</span></span>

<span data-ttu-id="3a28f-122">エクスポートしたデータの移行を成功させるには、ソース テーブルが同等のターゲット データ エンティティにマップされていることが必要です。</span><span class="sxs-lookup"><span data-stu-id="3a28f-122">Successful migration of exported data requires that a source table be mapped to an equivalent target data entity.</span></span> <span data-ttu-id="3a28f-123">各テーブルのソースフィールドとターゲットフィールドの自動マッピングを可能にする Microsoft Excel マッピングファイルを使用してマッピングを設定します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-123">You set up the mapping by using a Microsoft Excel mapping file that allows for automatic mapping of the source and target fields of each table.</span></span> <span data-ttu-id="3a28f-124">マッピング ファイルには、新しいデータ エンティティのスキーマからのデータと、いくつかのテーブルで必要な既定のデータも含まれます。</span><span class="sxs-lookup"><span data-stu-id="3a28f-124">The mapping file also includes the data from the schema of the new data entities and the default data that is required in some tables.</span></span>

<span data-ttu-id="3a28f-125">AX 2009 からデータを移行する前に、移行の要件を満たすために次のタスクを完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a28f-125">Before you can migrate data from AX 2009, you must complete the following tasks to meet the migration requirements:</span></span>

- <span data-ttu-id="3a28f-126">選択した法人に基づいてに入力されたソース分析コードに対応する目標の分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-126">Select target dimensions that correspond to the source dimensions that are populated based on the selected legal entities.</span></span>
- <span data-ttu-id="3a28f-127">選択した法人に含まれている在庫分析コードを確認します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-127">Review the inventory dimensions that are included with the selected legal entities.</span></span>
- <span data-ttu-id="3a28f-128">各法人の勘定科目表を選択するか、単一の勘定科目に複数の法人を連結します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-128">Select the chart of accounts for each legal entity, or consolidate multiple legal entities into a single chart of accounts.</span></span>
- <span data-ttu-id="3a28f-129">基本的な元帳設定を実行します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-129">Complete the basic ledger setup.</span></span>
- <span data-ttu-id="3a28f-130">フィールドの拡張データ型 (EDT) に基づき、ソース データにデータ変換を適用します。</span><span class="sxs-lookup"><span data-stu-id="3a28f-130">Apply data conversions to the source data, based on the extended data type (EDT) of the field.</span></span>
