---
title: "データのインポート/エクスポート フレームワークのユーザー ガイド (AX 2012)"
description: "このトピックでは、Dynamics AX でデータ インポート/エクスポート フレームワーク (DIXF) を使用する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18121
ms.assetid: 393101f6-54b0-4198-a31c-3ff3125f33da
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f2fddfc5717cdb42df3a764b47ca2a8d52638347
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="data-importexport-framework-user-guide-ax-2012"></a><span data-ttu-id="cb1dd-103">データのインポート/エクスポート フレームワークのユーザー ガイド (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="cb1dd-103">Data import/export framework user guide (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb1dd-104">さまざまなバージョンのデータのインポート/エクスポート フレームワークを利用できます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-104">Various versions of the Data Import/Export Framework are available.</span></span> <span data-ttu-id="cb1dd-105">使用するバージョンは、ご使用の環境で実行する Microsoft Dynamics AX のバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-105">The version that you use depends on the version of Microsoft Dynamics AX that you run in your environment:</span></span>

-   <span data-ttu-id="cb1dd-106">Microsoft Dynamics AX 2012 R3 で、そのリリースに含まれるデータのインポート/エクスポート フレームワークのバージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-106">For Microsoft Dynamics AX 2012 R3, use the version of the Data Import/Export Framework that is included in that release.</span></span>
-   <span data-ttu-id="cb1dd-107">Microsoft Dynamics AX 2012 R2 で、Microsoft Dynamics AX 2012 R2 の累積更新 7 で利用できるデータのインポート/エクスポート フレームワークのバージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-107">For Microsoft Dynamics AX 2012 R2, use the version of the Data Import/Export Framework that is available in cumulative update 7 for Microsoft Dynamics AX 2012 R2.</span></span>
-   <span data-ttu-id="cb1dd-108">AX 2012 または Microsoft Dynamics AX 2012 Feature Pack で、[Lifecycle Services のダウンロード可能ツール (旧 InformationSource)](lcs-downloadable-tools-formerly-informationsource.md) から使用可能なデータのインポート/エクスポート フレームワークのバージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-108">For AX 2012 or Microsoft Dynamics AX 2012 Feature Pack, use the version of the Data Import/Export Framework that is available from the [Lifecycle Services Downloadable Tools (formerly on InformationSource)](lcs-downloadable-tools-formerly-informationsource.md).</span></span>

| <span data-ttu-id="cb1dd-109">**メモ**</span><span class="sxs-lookup"><span data-stu-id="cb1dd-109">**Note**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1dd-110">累積的な更新 7 のデータのインポート/エクスポート フレームワークおよび and Microsoft Dynamics AX 2012 R3 には、LCS からダウンロードできるバージョンでは使用できない機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-110">The versions of the Data Import/Export Framework in cumulative update 7 and Microsoft Dynamics AX 2012 R3 include functionality that is not available in the version that is available for download from LCS.</span></span> <span data-ttu-id="cb1dd-111">詳細については、[データのインポート/エクスポート フレームワークを使用する移行データ (DIXF, DMF)](migrate-data-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-111">For more information, see [Migrating data using the Data import/export framework (DIXF, DMF)](migrate-data-dixf.md).</span></span> |

## <a name="architecture"></a><span data-ttu-id="cb1dd-112">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="cb1dd-112">Architecture</span></span>
<span data-ttu-id="cb1dd-113">次の図は、データ インポート/エクスポート フレームワークのアーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-113">The following diagram shows the architecture of the Data Import/Export Framework.</span></span> 

![データ移行フレームワークのアーキテクチャ図](./media/dmfarchitecture.png) 

<span data-ttu-id="cb1dd-115">データのインポート/エクスポート フレームワークは、対象のテーブルが置かれている Microsoft Dynamics AX データベースに各エンティティのステージング テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-115">The Data Import/Export Framework creates a staging table for each entity in the Microsoft Dynamics AX database where the target table resides.</span></span> <span data-ttu-id="cb1dd-116">移行中のデータは、まずステージング テーブルに移動されます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-116">Data that is being migrated is first moved to the staging table.</span></span> <span data-ttu-id="cb1dd-117">そこでは、データを検証し、必要なクリーンアップまたは変換を実行できます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-117">There, you can verify the data, and perform any cleanup or conversion that is required.</span></span> <span data-ttu-id="cb1dd-118">その後、データをターゲット テーブルに移動またはエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-118">You can then move the data to the target table or export it.</span></span>

## <a name="the-importexport-process"></a><span data-ttu-id="cb1dd-119">プロセスをインポート/エクスポート</span><span class="sxs-lookup"><span data-stu-id="cb1dd-119">The Import/Export Process</span></span>
<span data-ttu-id="cb1dd-120">次の図は、Microsoft Dynamics AX でデータをインポートまたはエクスポートするために必要な手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-120">The following diagram shows the steps that are required to import or export data in Microsoft Dynamics AX.</span></span> ![データ移行フレームワークのコンフィギュレーション図](./media/dmfconfiguration.png)
1.  <span data-ttu-id="cb1dd-122">エクスポートまたはインポートするデータのソースを特定し、そのデータのソース データ形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-122">Determine the source of the data to export or import, and create a source data format for the data.</span></span> <span data-ttu-id="cb1dd-123">エクスポートについては、ソースは **AX** です。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-123">For export, the source is **AX**.</span></span> <span data-ttu-id="cb1dd-124">インポートについては、次のソースのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-124">For import, you can use any of the following sources:</span></span>
    -   <span data-ttu-id="cb1dd-125">**AX** - 別の Microsoft Dynamics AX インスタンスからデータをインポートします。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-125">**AX** – Import data from another Microsoft Dynamics AX instance.</span></span>
    -   <span data-ttu-id="cb1dd-126">**ODBC** – Microsoft SQL Server または Microsoft Access などの別のデータベースからデータをインポートします。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-126">**ODBC** – Import data from another database, such as Microsoft SQL Server or Microsoft Access.</span></span>
    -   <span data-ttu-id="cb1dd-127">**ファイル** – 固定長からデータをインポートまたはテキスト ファイル、XML ファイルまたは Microsoft Excel ファイルの区切り。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-127">**File** – Import data from a fixed-width or delimited text file, XML file, or Microsoft Excel file.</span></span>

    <span data-ttu-id="cb1dd-128">ソース データ フォーマットを作成する方法の詳細については、[データのインポート/エクスポート フレームワークを使用する移行データ (DIXF、DMF)](migrate-data-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-128">For more information about how to create a source data format, see [Migrating data using the Data import/export framework (DIXF, DMF)](migrate-data-dixf.md).</span></span>
2.  <span data-ttu-id="cb1dd-129">データに関連付けるエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-129">Determine which entity to associate with the data.</span></span> <span data-ttu-id="cb1dd-130">このエンティティは、エクスポート データのソースまたはインポート データのターゲットのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-130">This entity is either the source of the export data or the target for the import data.</span></span> <span data-ttu-id="cb1dd-131">既存のエンティティを使用、またはカスタム エンティティを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-131">You can use an existing entity or create a custom entity.</span></span> <span data-ttu-id="cb1dd-132">利用可能なエンティティの一覧については、[データのインポート/エクスポート フレームワークのエンティティ (DIXF、DMF)](entities-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-132">For a list of available entities, see [Data import/export framework entities (DIXF, DMF)](entities-dixf.md).</span></span> <span data-ttu-id="cb1dd-133">カスタム エンティティを作成する方法の詳細については、[データのインポート/エクスポート フレームワークのカスタム ターゲット エンティティを作成する (DIXF、DMF)](create-custom-target-entity-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-133">For information about how to create a custom entity, see [Create a custom target entity for the Data import/export framework (DIXF, DMF)](create-custom-target-entity-dixf.md).</span></span>
3.  <span data-ttu-id="cb1dd-134">どのエンティティをインポートまたはエクスポートするかを決定し、すべてのエンティティを処理グループに入れます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-134">Determine which entities should be imported or exported together, and put all these entities in a processing group.</span></span> <span data-ttu-id="cb1dd-135">処理グループは、順番に処理する必要があるか、論理的にグループ化できる一連のエンティティです。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-135">A processing group is a set of entities that must be processed in a sequence, or that can logically be grouped together.</span></span> <span data-ttu-id="cb1dd-136">処理グループ内のエンティティは、一緒にエクスポートされるか、ソースからステージングに、次にステージングからターゲットにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-136">The entities in a processing group are exported together, or they are imported together from source to staging and then from staging to target.</span></span> <span data-ttu-id="cb1dd-137">処理グループでは、各エンティティをソース データの形式とも関連付けます。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-137">In a processing group, you also associate each entity with a source data format.</span></span> <span data-ttu-id="cb1dd-138">処理グループを作成する方法の詳細については、[データのインポート/エクスポート フレームワークを使用する移行データ (DIXF、DMF)](migrate-data-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-138">For more information about how to create a processing group, see [Migrating data using the Data import/export framework (DIXF, DMF)](migrate-data-dixf.md).</span></span>
4.  <span data-ttu-id="cb1dd-139">データのエクスポートまたはインポートするには、処理グループのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-139">Use the processing group options to either import or export data.</span></span> <span data-ttu-id="cb1dd-140">インスポートについては、必要に応じて、データをクリーンアップまたは変換できるステージング テーブルに、データをまず移動します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-140">For import, you first import the data to a staging table, where you can clean or transform the data as you require.</span></span> <span data-ttu-id="cb1dd-141">データが正確で表示され、参照データが正しくマップされていることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-141">You should validate that the data appears accurate, and that the reference data is mapped correctly.</span></span> <span data-ttu-id="cb1dd-142">次に、ステージング テーブルからターゲット テーブルにデータを移行します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-142">You then migrate the data from the staging table to the target table.</span></span> <span data-ttu-id="cb1dd-143">エンティティが対象のテーブルに正確に表示されることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-143">You should validate that the entity appears accurate in the target table.</span></span>

    | <span data-ttu-id="cb1dd-144">**重要**</span><span class="sxs-lookup"><span data-stu-id="cb1dd-144">**Important**</span></span>                                                                                                                                            |
    |----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="cb1dd-145">ステージング データにはビジネス情報が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-145">The staging data might contain business information.</span></span> <span data-ttu-id="cb1dd-146">したがって、移行が完了した後でステージング データを削除することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-146">Therefore, we strongly recommend that you delete the staging data after the migration is completed.</span></span> |

    <span data-ttu-id="cb1dd-147">エクスポートについては、必要に応じて、データをクリーンアップまたは変換できるステージング テーブルに、ソースからデータも移動します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-147">For export, you also move the data from the source to a staging table, where you can clean or transform the data as you require.</span></span> <span data-ttu-id="cb1dd-148">次に、Microsoft Dynamics AX またはファイルのいずれかに、データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-148">You then export the data either to Microsoft Dynamics AX or to a file.</span></span> <span data-ttu-id="cb1dd-149">最初のオプションは、別の Microsoft Dynamics AX インスタンスにインポートできるように、データの .dat ファイルと .def ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-149">The first option creates a .dat file and a .def file for the data, so that it can be imported into another Microsoft Dynamics AX instance.</span></span> <span data-ttu-id="cb1dd-150">2 番目のオプションは、データのフラット ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1dd-150">The second option creates a flat file for the data.</span></span>






