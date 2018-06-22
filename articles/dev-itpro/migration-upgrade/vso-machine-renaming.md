---
title: "Visual Studio Team Services へのアクセスを有効化するには、ローカル環境の名前を変更してください"
description: "複数のコンピューターにまたがる VSTS プロジェクトにアクセスするには、ローカル開発 VM の名前変更が必要です。"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 815f7efc82b22df1c90fbb790f45c792235da680
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="rename-a-local-environment-to-enable-access-to-visual-studio-team-services"></a><span data-ttu-id="d1148-103">Visual Studio Team Services へのアクセスを有効化するには、ローカル環境の名前を変更してください</span><span class="sxs-lookup"><span data-stu-id="d1148-103">Rename a local environment to enable access to Visual Studio Team Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1148-104">複数のコンピューターにまたがる VSTS プロジェクトにアクセスするには、ローカル開発 VM の名前変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="d1148-104">Renaming a local development VMs is required in order to access a VSTS project across multiple machines.</span></span>

<span data-ttu-id="d1148-105">Visual Studio Team Services (VSTS) (旧名称は Visual Studio Online または VSO) はバージョン コントロールのために必要です。</span><span class="sxs-lookup"><span data-stu-id="d1148-105">Visual Studio Team Services (VSTS) (formerly known as Visual Studio Online or VSO) is needed for version control.</span></span> <span data-ttu-id="d1148-106">開発トポロジでは、複数の VM が同じコンピューター名である場合、同じ VSTS プロジェクトにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="d1148-106">In development topologies, multiple VMs cannot access the same VSTS project if they have the same machine name.</span></span> <span data-ttu-id="d1148-107">VSTS はマシン名を ID として使用します。</span><span class="sxs-lookup"><span data-stu-id="d1148-107">VSTS uses the machine name for identification.</span></span> <span data-ttu-id="d1148-108">Microsoft Lifecycle Services (LCS) からローカル VM で開発する場合は、問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1148-108">If you are developing on local VMs downloaded from Microsoft Lifecycle Services (LCS), you may encounter issues.</span></span>

- <span data-ttu-id="d1148-109">この問題を回避するには、開発を開始する前にマシンの名前を変更してリブートし、VSTS に接続します。</span><span class="sxs-lookup"><span data-stu-id="d1148-109">To work around this, rename and reboot the machine before you start development, then connect to VSTS.</span></span>
- <span data-ttu-id="d1148-110">これらを実行した後、SQL Server レポート サーバーもコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1148-110">After you do this you will also need to configure the SQL Server Reporting Server.</span></span> <span data-ttu-id="d1148-111">これを行うには、SQL Server レポート サーバーのデータベース接続文字列で SQL Server 名を (localhost) に変更します。</span><span class="sxs-lookup"><span data-stu-id="d1148-111">To do that, change the SQL Server Name to (localhost) in the SQL Server Report Server Database connection string.</span></span>

  <span data-ttu-id="d1148-112">[![4](./media/4.png)](./media/4.png)</span><span class="sxs-lookup"><span data-stu-id="d1148-112">[![4](./media/4.png)](./media/4.png)</span></span>




