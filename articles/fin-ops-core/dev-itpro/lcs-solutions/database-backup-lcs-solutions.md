---
title: Finance and Operations アプリのデータベースのバックアップ
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要なデータベースのバックアップに関する情報を提供します。
author: kfend
ms.date: 04/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 196833
ms.assetid: fc0f06e8-1a20-45f7-ae98-ee074fe1f030
ms.search.region: Global
ms.author: omarc
ms.openlocfilehash: b7edc94ea71c2a72a064c100db2590b23df20f8e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750354"
---
# <a name="back-up-the-databases-for-finance-and-operations-apps"></a><span data-ttu-id="27989-103">Finance and Operations アプリのデータベースのバックアップ</span><span class="sxs-lookup"><span data-stu-id="27989-103">Back up the databases for Finance and Operations apps</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27989-104">Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージには、Finance and Operations アプリ データベースのバックアップが必要です。</span><span class="sxs-lookup"><span data-stu-id="27989-104">A backup of theFinance and Operations apps database is required for your Microsoft Dynamics Lifecycle Services (LCS) solution package.</span></span> <span data-ttu-id="27989-105">データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="27989-105">When you back up the database, you must include the master, reference, and transactional data that is specific to your solution and industry.</span></span> <span data-ttu-id="27989-106">このデータは販売前のデモ展開に使用されます。</span><span class="sxs-lookup"><span data-stu-id="27989-106">This data will be used for your pre-sales demo deployments.</span></span>

<span data-ttu-id="27989-107">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="27989-107">On demo or development environments, the database is typically named AXDBRain.</span></span> <span data-ttu-id="27989-108">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27989-108">Your database backup should be no larger than 15 gigabytes (GB).</span></span> <span data-ttu-id="27989-109">それ以外の場合は 、LCS でアセット ライブラリにデータベースをアップロードしようとすると、タイムアウト エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="27989-109">Otherwise, a time-out error might occur when you try to upload the database to the Asset library in LCS.</span></span> 

<span data-ttu-id="27989-110">Microsoft SQL Server Management Studio で、データベースのバックアップを圧縮するには、**データベースのバックアップ** ページの **バックアップ圧縮を設定** フィールドで、**バックアップの圧縮** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27989-110">To compress your database backup, in Microsoft SQL Server Management Studio, on the **Back Up Database** page, in the **Set backup compression** field, select **Compress backup**.</span></span>

<span data-ttu-id="27989-111">[![セット バックアップ圧縮フィールドで選択されたバックアップを圧縮](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span><span class="sxs-lookup"><span data-stu-id="27989-111">[![Compress backup selected in the Set backup compression field](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span></span>

<span data-ttu-id="27989-112">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="27989-112">On demo or development environments, the database is typically called AXDBRain.</span></span> <span data-ttu-id="27989-113">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27989-113">Your database backup should be no larger than 15 gigabyte (GB).</span></span> <span data-ttu-id="27989-114">データベースが大きい場合、Lifecycle Services (LCS) のアセットライブラリにデータベースをアップロードする際に、タイムアウトエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="27989-114">If your database is larger, a timeout error may occur when you try to upload the database to the Asset library in Lifecycle Services (LCS).</span></span> 
  
<span data-ttu-id="27989-115">SQL Server Management Studio で、データベースのバックアップを圧縮するには、 **データベースのバックアップ** ページの **バックアップ圧縮を設定する** フィールドで、 **バックアップを圧縮する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27989-115">To compress your database backup, in SQL Server Management Studio, on the **Back Up Database** page, in the **Set backup compression** field, select **Compress backup**.</span></span> 

<span data-ttu-id="27989-116">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span><span class="sxs-lookup"><span data-stu-id="27989-116">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27989-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="27989-117">Additional resources</span></span>

[<span data-ttu-id="27989-118">AppSource でアプリを公開するための要件</span><span class="sxs-lookup"><span data-stu-id="27989-118">Requirements for publishing apps on AppSource</span></span>](lcs-solutions-app-source.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]