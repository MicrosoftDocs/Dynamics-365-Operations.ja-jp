---
title: "詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード"
description: "番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0fb86cd4264d5420c479e14f7eed41e480c88b63
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="4f1d6-103">詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード</span><span class="sxs-lookup"><span data-stu-id="4f1d6-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4f1d6-104">番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="4f1d6-105">次の手順で、口座取引明細書のインポート エンティティを MT940 形式をサポートするために追加します。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="4f1d6-106">以下をコンパイルして同期します:</span><span class="sxs-lookup"><span data-stu-id="4f1d6-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="4f1d6-107">複合エンティティ\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="4f1d6-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="4f1d6-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="4f1d6-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="4f1d6-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="4f1d6-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="4f1d6-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="4f1d6-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="4f1d6-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="4f1d6-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="4f1d6-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="4f1d6-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="4f1d6-113">データ管理\\data projects.</span><span class="sxs-lookup"><span data-stu-id="4f1d6-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="4f1d6-114">MT940 のプロジェクトのインポートを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="4f1d6-115">XSLT に変更します。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-115">Change XSLT.</span></span>
            -   <span data-ttu-id="4f1d6-116">[**マップの表示**]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-116">Click **View map**.</span></span>
            -   <span data-ttu-id="4f1d6-117">口座取引明細書ドキュメントの[**表示のマップ**]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="4f1d6-118">[**変換**]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="4f1d6-119">BankReconiliation-to-Composite.xslt ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="4f1d6-120">BankReconiliation-to-Composite.xsl の新しいバージョンを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="4f1d6-121">[**ソース データ**] レイアウトで**番号順序**を公開します。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="4f1d6-122">ソースデータ形式 = XML-Element</span><span class="sxs-lookup"><span data-stu-id="4f1d6-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="4f1d6-123">エンティティ名 = 口座取引明細書</span><span class="sxs-lookup"><span data-stu-id="4f1d6-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="4f1d6-124">データ ファイルのアップロード = 新しいバージョンの SampleBankCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="4f1d6-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="4f1d6-125">既存のファイルを上書きするには、[**はい**]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="4f1d6-126">新しいマップを生成するためには、[**はい**]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="4f1d6-127">[**SequenceNumber**] がマップされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="4f1d6-128">明細書エンティティの[**マップの表示**]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="4f1d6-129">[**SequenceNumber**] がソースからステージングにマップされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="4f1d6-130">新しい明細書をインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f1d6-130">Import the new statement.</span></span>





