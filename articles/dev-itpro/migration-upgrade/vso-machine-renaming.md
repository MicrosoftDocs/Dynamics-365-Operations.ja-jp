---
title: "Azure DevOps にアクセスするためのローカル環境の名前変更"
description: "複数のコンピューターにまたがる Azure DevOps プロジェクトにアクセスするには、ローカル開発 VM の名前変更が必要です。"
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25911
ms.assetid: 4f5ff29b-9ae5-4ba2-8b6e-1e5d94e004b3
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d22fe0c9a38026350c839d1d7d35835bfc77d995
ms.openlocfilehash: c2d40d2efd0c5c6fa02dea93ab9a3e0e066a8918
ms.contentlocale: ja-jp
ms.lasthandoff: 09/17/2018

---

# <a name="rename-a-local-environment-to-access-azure-devops"></a><span data-ttu-id="0dea4-103">Azure DevOps にアクセスするためのローカル環境の名前変更</span><span class="sxs-lookup"><span data-stu-id="0dea4-103">Rename a local environment to access Azure DevOps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0dea4-104">複数のコンピューターにまたがる Azure DevOps プロジェクトにアクセスするには、ローカル開発 VM の名前変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="0dea4-104">Renaming a local development VMs is required in order to access a Azure DevOps project across multiple machines.</span></span>

<span data-ttu-id="0dea4-105">Azure DevOps (旧名称は Visual Studio Online または VSO) はバージョン コントロールのために必要です。</span><span class="sxs-lookup"><span data-stu-id="0dea4-105">Azure DevOps (formerly known as Visual Studio Online or VSO) is needed for version control.</span></span> <span data-ttu-id="0dea4-106">開発トポロジでは、複数の VM が同じコンピューター名である場合、同じ Azure DevOps プロジェクトにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="0dea4-106">In development topologies, multiple VMs cannot access the same Azure DevOps project if they have the same machine name.</span></span> <span data-ttu-id="0dea4-107">Azure DevOps はマシン名を ID として使用します。</span><span class="sxs-lookup"><span data-stu-id="0dea4-107">Azure DevOps uses the machine name for identification.</span></span> <span data-ttu-id="0dea4-108">Microsoft Lifecycle Services (LCS) からローカル VM で開発する場合は、問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0dea4-108">If you are developing on local VMs downloaded from Microsoft Lifecycle Services (LCS), you may encounter issues.</span></span>

- <span data-ttu-id="0dea4-109">この問題を回避するには、開発を開始する前にマシンの名前を変更してリブートし、Azure DevOps に接続します。</span><span class="sxs-lookup"><span data-stu-id="0dea4-109">To work around this, rename and reboot the machine before you start development, then connect to Azure DevOps.</span></span>
- <span data-ttu-id="0dea4-110">これらを実行した後、SQL Server レポート サーバーもコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0dea4-110">After you do this you will also need to configure the SQL Server Reporting Server.</span></span> <span data-ttu-id="0dea4-111">これを行うには、SQL Server レポート サーバーのデータベース接続文字列で SQL Server 名を (localhost) に変更します。</span><span class="sxs-lookup"><span data-stu-id="0dea4-111">To do that, change the SQL Server Name to (localhost) in the SQL Server Report Server Database connection string.</span></span>

  




