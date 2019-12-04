---
title: Finance and Operations アプリのデータベースのバックアップ
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要なデータベースのバックアップに関する情報を提供します。
author: kfend
manager: AnnBe
ms.date: 04/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Lifecycle Services
ms.custom: 196833
ms.assetid: fc0f06e8-1a20-45f7-ae98-ee074fe1f030
ms.search.region: Global
ms.author: omarc
ms.openlocfilehash: c94315c8bf202594f8b4d73cc920cccefad24a56
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811705"
---
# <a name="back-up-the-databases-for-finance-and-operations-apps"></a><span data-ttu-id="cb620-103">Finance and Operations アプリのデータベースのバックアップ</span><span class="sxs-lookup"><span data-stu-id="cb620-103">Back up the databases for Finance and Operations apps</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cb620-104">Finance and Operations アプリのデータベースのバックアップは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要です。</span><span class="sxs-lookup"><span data-stu-id="cb620-104">A backup of theFinance and Operations apps database is required for your Microsoft Dynamics Lifecycle Services (LCS) solution package.</span></span> <span data-ttu-id="cb620-105">データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb620-105">When you back up the database, you must include the master, reference, and transactional data that is specific to your solution and industry.</span></span> <span data-ttu-id="cb620-106">このデータは販売前のデモ展開に使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb620-106">This data will be used for your pre-sales demo deployments.</span></span>

<span data-ttu-id="cb620-107">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cb620-107">On demo or development environments, the database is typically named AXDBRain.</span></span> <span data-ttu-id="cb620-108">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb620-108">Your database backup should be no larger than 15 gigabytes (GB).</span></span> <span data-ttu-id="cb620-109">それ以外の場合は 、LCS でアセット ライブラリにデータベースをアップロードしようとすると、タイムアウト エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cb620-109">Otherwise, a time-out error might occur when you try to upload the database to the Asset library in LCS.</span></span> 

<span data-ttu-id="cb620-110">Microsoft SQL Server Management Studio で、データベースのバックアップを圧縮するには、**データベースのバックアップ** ページの**バックアップ圧縮を設定**フィールドで、**バックアップの圧縮**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb620-110">To compress your database backup, in Microsoft SQL Server Management Studio, on the **Back Up Database** page, in the **Set backup compression** field, select **Compress backup**.</span></span>

<span data-ttu-id="cb620-111">[![セット バックアップ圧縮フィールドで選択されたバックアップを圧縮](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span><span class="sxs-lookup"><span data-stu-id="cb620-111">[![Compress backup selected in the Set backup compression field](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span></span>

<span data-ttu-id="cb620-112">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cb620-112">On demo or development environments, the database is typically called AXDBRain.</span></span> <span data-ttu-id="cb620-113">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb620-113">Your database backup should be no larger than 15 gigabyte (GB).</span></span> <span data-ttu-id="cb620-114">データベースが大きい場合、Lifecycle Services (LCS) のアセットライブラリにデータベースをアップロードする際に、タイムアウトエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="cb620-114">If your database is larger, a timeout error may occur when you try to upload the database to the Asset library in Lifecycle Services (LCS).</span></span> 
  
<span data-ttu-id="cb620-115">SQL Server Management Studio で、データベースのバックアップを圧縮するには、 **データベースのバックアップ** ページの **バックアップ圧縮を設定する** フィールドで、 **バックアップを圧縮する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb620-115">To compress your database backup, in SQL Server Management Studio, on the **Back Up Database** page, in the **Set backup compression** field, select **Compress backup**.</span></span> 

<span data-ttu-id="cb620-116">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span><span class="sxs-lookup"><span data-stu-id="cb620-116">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb620-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cb620-117">Additional resources</span></span>

[<span data-ttu-id="cb620-118">AppSource でアプリを公開するための要件</span><span class="sxs-lookup"><span data-stu-id="cb620-118">Requirements for publishing apps on AppSource</span></span>](lcs-solutions-app-source.md)
