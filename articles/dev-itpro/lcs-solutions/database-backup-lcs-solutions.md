---
title: "LCS ソリューション データベースのバックアップ"
description: "LCS ソリューション パッケージには、Finance and Operations のデータベース バックアップが必要です。 データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。 これは、販売前のデモ展開に使用されます。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196833
ms.assetid: fc0f06e8-1a20-45f7-ae98-ee074fe1f030
ms.search.region: Global
ms.author: omarc
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 51d2da271f8be1527854d8bb00566b5ac4b67e3f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="back-up-database-for-an-lcs-solution"></a><span data-ttu-id="f243b-105">LCS ソリューション データベースのバックアップ</span><span class="sxs-lookup"><span data-stu-id="f243b-105">Back up database for an LCS solution</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f243b-106">LCS ソリューション パッケージには、Finance and Operations のデータベース バックアップが必要です。</span><span class="sxs-lookup"><span data-stu-id="f243b-106">A Finance and Operations database backup is required for your LCS solution package.</span></span> <span data-ttu-id="f243b-107">データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f243b-107">When you back up your database, you must include the master, reference, and transactional data that is specific to your solution and industry.</span></span> <span data-ttu-id="f243b-108">これは、販売前のデモ展開に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f243b-108">This will be used for your pre-sales demo deployments.</span></span> 

<span data-ttu-id="f243b-109">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f243b-109">On demo or development environments, the database is typically called AXDBRain.</span></span> <span data-ttu-id="f243b-110">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f243b-110">Your database backup should be no larger than 15 gigabyte (GB).</span></span> <span data-ttu-id="f243b-111">データベースが大きい場合、Lifecycle Services (LCS) で<strong>アセット ライブラリ**にデータベースをアップロードしようとすると、タイムアウト エラーが発生する場合があります。データベース バックアップを圧縮するには、SQL Server Management Studio で、**データベースのバックアップ</strong> ページの<strong>バックアップ圧縮の設定</strong>フィールドで、<strong>バックアップの圧縮</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="f243b-111">If your database is larger, a timeout error may occur when you try to upload the database to the <strong>Asset library **in Lifecycle Services (LCS). To compress your database backup, in SQL Server Management Studio, on the **Back Up Database</strong> page, in the <strong>Set backup compression</strong> field, select <strong>Compress backup</strong>.</span></span> 

<span data-ttu-id="f243b-112">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span><span class="sxs-lookup"><span data-stu-id="f243b-112">[![databasebackup01](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</span></span>

<a name="additional-resources"></a><span data-ttu-id="f243b-113">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f243b-113">Additional resources</span></span>
--------

[<span data-ttu-id="f243b-114">AppSource 向け LCS ソリューション ホームページ</span><span class="sxs-lookup"><span data-stu-id="f243b-114">LCS Solutions for AppSource home page</span></span>](lcs-solutions-app-source.md)




