---
title: Finance and Operations ソリューションのデータベースのバックアップ
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要なデータベースのバックアップに関する情報を提供します。
author: kfend
manager: AnnBe
ms.date: 04/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196833
ms.assetid: fc0f06e8-1a20-45f7-ae98-ee074fe1f030
ms.search.region: Global
ms.author: omarc
ms.openlocfilehash: 4c47453b0b247fc9553e143f4d24cb45afeffbaf
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "377866"
---
# <a name="back-up-the-databases-for-finance-and-operations-solutions"></a><span data-ttu-id="d66a1-103">Finance and Operations ソリューションのデータベースのバックアップ</span><span class="sxs-lookup"><span data-stu-id="d66a1-103">Back up the databases for Finance and Operations solutions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d66a1-104">バックアップを保存した Microsoft Dynamics 365 for Finance and Operations データベースに必要な Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージします。</span><span class="sxs-lookup"><span data-stu-id="d66a1-104">A backup of the Microsoft Dynamics 365 for Finance and Operations database is required for your Microsoft Dynamics Lifecycle Services (LCS) solution package.</span></span> <span data-ttu-id="d66a1-105">データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d66a1-105">When you back up the database, you must include the master, reference, and transactional data that is specific to your solution and industry.</span></span> <span data-ttu-id="d66a1-106">このデータは販売前のデモ展開に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d66a1-106">This data will be used for your pre-sales demo deployments.</span></span>

<span data-ttu-id="d66a1-107">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d66a1-107">On demo or development environments, the database is typically named AXDBRain.</span></span> <span data-ttu-id="d66a1-108">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d66a1-108">Your database backup should be no larger than 15 gigabytes (GB).</span></span> <span data-ttu-id="d66a1-109">それ以外の場合は 、LCS でアセット ライブラリにデータベースをアップロードしようとすると、タイムアウト エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d66a1-109">Otherwise, a time-out error might occur when you try to upload the database to the Asset library in LCS.</span></span> <span data-ttu-id="d66a1-110">Microsoft SQL Server Management Studio で、データベースのバックアップを圧縮するには、**データベースのバックアップ** ページの**バックアップ圧縮を設定**フィールドで、**バックアップの圧縮**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d66a1-110">To compress your database backup, in Microsoft SQL Server Management Studio, on the **Back Up Database** page, in the **Set backup compression** field, select **Compress backup**.</span></span>

<a name="compress-backup-selected-in-the-set-backup-compression-fieldmediadatabasebackup01jpgmediadatabasebackup01jpg"></a><span data-ttu-id="d66a1-111">[![セット バックアップ圧縮フィールドで選択されたバックアップを圧縮](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span><span class="sxs-lookup"><span data-stu-id="d66a1-111">[![Compress backup selected in the Set backup compression field](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span></span>
=======
<span data-ttu-id="d66a1-112">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d66a1-112">On demo or development environments, the database is typically called AXDBRain.</span></span> <span data-ttu-id="d66a1-113">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d66a1-113">Your database backup should be no larger than 15 gigabyte (GB).</span></span> <span data-ttu-id="d66a1-114">データベースが大きい場合、Lifecycle Services (LCS) で<strong>アセット ライブラリ**にデータベースをアップロードしようとすると、タイムアウト エラーが発生する場合があります。データベース バックアップを圧縮するには、SQL Server Management Studio で、**データベースのバックアップ</strong> ページの<strong>バックアップ圧縮の設定</strong>フィールドで、<strong>バックアップの圧縮</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="d66a1-114">If your database is larger, a timeout error may occur when you try to upload the database to the <strong>Asset library \*\*in Lifecycle Services (LCS). To compress your database backup, in SQL Server Management Studio, on the \*\*Back Up Database</strong> page, in the <strong>Set backup compression</strong> field, select <strong>Compress backup</strong>.</span></span> 

<span data-ttu-id="d66a1-115">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span><span class="sxs-lookup"><span data-stu-id="d66a1-115">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d66a1-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d66a1-116">Additional resources</span></span>

[<span data-ttu-id="d66a1-117">AppSource の Dynamics 365 for Finance and Operations アプリを公開</span><span class="sxs-lookup"><span data-stu-id="d66a1-117">Publishing an App for Dynamics 365 for Finance and Operations in AppSource</span></span>](lcs-solutions-app-source.md)
