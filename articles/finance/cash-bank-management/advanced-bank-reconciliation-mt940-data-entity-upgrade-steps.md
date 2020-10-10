---
title: 詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード
description: 番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 65970cdac114b72363d2fbbc08766c99ace00b88
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899376"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="aceab-103">詳細な口座調整 MT940 のインポート – 複合データ エンティティのアップグレード</span><span class="sxs-lookup"><span data-stu-id="aceab-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aceab-104">番号順序は、MT940 形式をサポートするために、口座取引明細書のインポート エンティティに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aceab-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="aceab-105">次の手順で、口座取引明細書のインポート エンティティを MT940 形式をサポートするために追加します。</span><span class="sxs-lookup"><span data-stu-id="aceab-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="aceab-106">以下をコンパイルして同期します:</span><span class="sxs-lookup"><span data-stu-id="aceab-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="aceab-107">複合エンティティ\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="aceab-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="aceab-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="aceab-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="aceab-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="aceab-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="aceab-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="aceab-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="aceab-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="aceab-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="aceab-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="aceab-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="aceab-113">データ管理\\data projects.</span><span class="sxs-lookup"><span data-stu-id="aceab-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="aceab-114">MT940 のプロジェクトのインポートを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="aceab-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="aceab-115">XSLT に変更します。</span><span class="sxs-lookup"><span data-stu-id="aceab-115">Change XSLT.</span></span>
            -   <span data-ttu-id="aceab-116">**マップの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aceab-116">Click **View map**.</span></span>
            -   <span data-ttu-id="aceab-117">口座取引明細書ドキュメントの**表示のマップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aceab-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="aceab-118">**変換**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aceab-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="aceab-119">BankReconiliation-to-Composite.xslt ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="aceab-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="aceab-120">BankReconiliation-to-Composite.xsl の新しいバージョンを追加します。</span><span class="sxs-lookup"><span data-stu-id="aceab-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="aceab-121">**ソース データ**レイアウトで**番号順序**を公開します。</span><span class="sxs-lookup"><span data-stu-id="aceab-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="aceab-122">ソースデータ形式 = XML-Element</span><span class="sxs-lookup"><span data-stu-id="aceab-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="aceab-123">エンティティ名 = 口座取引明細書</span><span class="sxs-lookup"><span data-stu-id="aceab-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="aceab-124">データ ファイルのアップロード = 新しいバージョンの SampleBankCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="aceab-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="aceab-125">既存のファイルを上書きするには、**はい**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aceab-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="aceab-126">新しいマップを生成するためには、**はい**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aceab-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="aceab-127">**SequenceNumber** がマップされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="aceab-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="aceab-128">明細書エンティティの**マップの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aceab-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="aceab-129">**SequenceNumber** がソースからステージングにマップされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="aceab-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="aceab-130">新しい明細書をインポートします。</span><span class="sxs-lookup"><span data-stu-id="aceab-130">Import the new statement.</span></span>




