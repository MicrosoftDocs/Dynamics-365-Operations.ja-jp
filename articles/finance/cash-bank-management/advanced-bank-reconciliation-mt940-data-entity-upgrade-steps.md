---
title: 詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード
description: 番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6534cc0835eabe91ab485e1d71412885d12123f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827437"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="e7749-103">詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード</span><span class="sxs-lookup"><span data-stu-id="e7749-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7749-104">番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7749-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="e7749-105">次の手順で、口座取引明細書のインポート エンティティを MT940 形式をサポートするために追加します。</span><span class="sxs-lookup"><span data-stu-id="e7749-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="e7749-106">以下をコンパイルして同期します:</span><span class="sxs-lookup"><span data-stu-id="e7749-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="e7749-107">複合エンティティ\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="e7749-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="e7749-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="e7749-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="e7749-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="e7749-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="e7749-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="e7749-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="e7749-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="e7749-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="e7749-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="e7749-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="e7749-113">データ管理\\data projects.</span><span class="sxs-lookup"><span data-stu-id="e7749-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="e7749-114">MT940 のプロジェクトのインポートを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="e7749-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="e7749-115">XSLT に変更します。</span><span class="sxs-lookup"><span data-stu-id="e7749-115">Change XSLT.</span></span>
            -   <span data-ttu-id="e7749-116">**マップの表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7749-116">Click **View map**.</span></span>
            -   <span data-ttu-id="e7749-117">口座取引明細書ドキュメントの **表示のマップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7749-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="e7749-118">**変換** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7749-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="e7749-119">BankReconiliation-to-Composite.xslt ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="e7749-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="e7749-120">BankReconiliation-to-Composite.xsl の新しいバージョンを追加します。</span><span class="sxs-lookup"><span data-stu-id="e7749-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="e7749-121">**ソース データ** レイアウトで **番号順序** を公開します。</span><span class="sxs-lookup"><span data-stu-id="e7749-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="e7749-122">ソースデータ形式 = XML-Element</span><span class="sxs-lookup"><span data-stu-id="e7749-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="e7749-123">エンティティ名 = 口座取引明細書</span><span class="sxs-lookup"><span data-stu-id="e7749-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="e7749-124">データ ファイルのアップロード = 新しいバージョンの SampleBankCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="e7749-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="e7749-125">既存のファイルを上書きするには、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7749-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="e7749-126">新しいマップを生成するためには、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7749-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="e7749-127">**SequenceNumber** がマップされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e7749-127">Verify that S **equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="e7749-128">明細書エンティティの **マップの表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7749-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="e7749-129">**SequenceNumber** がソースからステージングにマップされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="e7749-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="e7749-130">新しい明細書をインポートします。</span><span class="sxs-lookup"><span data-stu-id="e7749-130">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]