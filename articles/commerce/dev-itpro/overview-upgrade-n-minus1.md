---
title: Commerce のアップグレードおよび N-1 のサポート
description: Dynamics 365 Commerce のリリースで、アップグレードと N-1 サポートが有効になりました。 N-1 のサポートによって、AX 2012 R3 CU10 を実行する店舗を持つ顧客は、アップグレード後に Dynamics 365 Commerce headquarters で作業できます。
author: athinesh99
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.service: Dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 44351
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2017-07-31
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 8d2855d7d8e21e8a5efcd012f1d7cd8eb5704495
ms.sourcegitcommit: d64a07748bdd7c85877cfe0343bee952f235f38e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2020
ms.locfileid: "3457182"
---
# <a name="upgrade-and-n-1-support-for-commerce"></a><span data-ttu-id="3c6ab-104">Commerce のアップグレードおよび N-1 のサポート</span><span class="sxs-lookup"><span data-stu-id="3c6ab-104">Upgrade and N-1 support for Commerce</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c6ab-105">Microsoft Dynamics 365 Retail の 2017年7月のリリースでは、アップグレードと N-1 の対応が有効となりました。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-105">Upgrade and N-1 support have been enabled in the July 2017 release of Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="3c6ab-106">N-1 のサポートによって、Microsoft Dynamics AX 2012 R3 累積更新プログラム 10 (CU10) を実行する店舗を持つ顧客は、アップグレード後にバックオフィスで作業できます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-106">N-1 support lets customers who have stores that run Microsoft Dynamics AX 2012 R3 Cumulative Update 10 (CU10) work with Headquarters after an upgrade.</span></span> <span data-ttu-id="3c6ab-107">アップグレードと N-1 サポートの主な目的は、AX 2012 R3 の顧客がクラウドの利点を活用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-107">The main purpose of upgrade and N-1 support is to let AX 2012 R3 customers take advantage of the benefits of the cloud.</span></span>

<span data-ttu-id="3c6ab-108">次の機能を使用すると、顧客はシームレスにアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-108">The following features let customers upgrade in a seamless manner:</span></span>

- <span data-ttu-id="3c6ab-109">アップグレード プロセスを通じて、AX 2012 R3 からバックオフィスへのデータベース アップグレードを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-109">Users can now perform database upgrade from AX 2012 R3 to Headquarters through the upgrade process.</span></span>
- <span data-ttu-id="3c6ab-110">AX 2012 R3 CU10 のコンポーネントを使用して店舗を運営することができます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-110">Users can operate their stores by using the components of AX 2012 R3 CU10.</span></span>
- <span data-ttu-id="3c6ab-111">アップグレード前とアップグレード後のチェックリストの検証は、アップグレード プロセスに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-111">Pre-upgrade and post-upgrade checklist validations are built into the upgrade process.</span></span>
- <span data-ttu-id="3c6ab-112">アップグレード プロセスでは、エラー処理とメッセージングが強化されているため、顧客は問題を迅速にデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-112">The upgrade process has enhanced error handling and messaging, so that customers can quickly debug issues.</span></span>
- <span data-ttu-id="3c6ab-113">ユーザーは、ツールを使用して、既存のバックオフィスのカスタムの X++ コードを、そのバックオフィスのアップグレードされたバージョンに移行することができます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-113">Users can use tools to bring forward custom X++ code in their existing Headquarters to the upgraded version of the headquarters.</span></span>

<span data-ttu-id="3c6ab-114">アップグレード手順は、Retail を最新バージョンにアップグレードする手順とほぼ同じです。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-114">The upgrade procedure is largely the same as the procedure for upgrading Retail to the latest version.</span></span> <span data-ttu-id="3c6ab-115">一般に、アップグレードに関する詳細については、「[AX 2012 から Dynamics 365 Retail へのアップグレードの概要](../../dev-itpro/migration-upgrade/upgrade-overview-2012.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-115">For details about upgrade in general, see [Upgrade overview: AX 2012 to Dynamics 365 Retail](../../dev-itpro/migration-upgrade/upgrade-overview-2012.md).</span></span>

<span data-ttu-id="3c6ab-116">計画的なダウンタイムが必要です。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-116">Planned downtime is required.</span></span> <span data-ttu-id="3c6ab-117">アップグレード分析を最初に行います。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-117">Upgrade analysis is done first.</span></span> <span data-ttu-id="3c6ab-118">アップグレード分析は、Microsoft Dynamics AX 2012 データベースに対して実行され、Microsoft Dynamics Lifecycle Services (LCS) 診断サービスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-118">The upgrade analysis runs against the Microsoft Dynamics AX 2012 database and is based on the Microsoft Dynamics Lifecycle Services (LCS) Diagnostic service.</span></span> <span data-ttu-id="3c6ab-119">このステップでは、アップグレードをより迅速かつ低コストで行うための作業を特定します。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-119">This step identifies tasks that can help make upgrade faster and less expensive.</span></span> <span data-ttu-id="3c6ab-120">また、必要な SQL 構成、データ バックオフィス クリーンアップ、推奨されない機能を識別します。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-120">It also identifies the required SQL configuration, data headquarters cleanup, and deprecated features.</span></span>
  
<span data-ttu-id="3c6ab-121">その後、実際のデータ アップグレード プロセスが発生します。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-121">The actual data upgrade process then occurs.</span></span> <span data-ttu-id="3c6ab-122">AX 2012 データベースは、Microsoft Azure SQL データベースに移動され、データ アップグレード パッケージは runbook プロセスを通じて通常どおり実行されます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-122">The AX 2012 database is moved to Microsoft Azure SQL Database, and then the data upgrade package is run as usual, through the runbook process.</span></span> <span data-ttu-id="3c6ab-123">アップグレードの検証が完了します。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-123">Upgrade validation is then done.</span></span> <span data-ttu-id="3c6ab-124">検証ツールは、使用される前にアップグレードされた環境に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-124">A validation tool is run against the upgraded environment before it's used.</span></span> <span data-ttu-id="3c6ab-125">このツールは自動スモーク テストを実行して、サービスが動作してアクセス可能なこと、行数の一致、財務と在庫の調整などを検証します。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-125">This tool does an automated smoke test to verify that the service is running and accessible, row counts match, financials and inventory reconcile, and so on.</span></span>
 
<span data-ttu-id="3c6ab-126">チャネルのアップグレード後構成のほとんどにおいて、手動での手順をほぼ必要としません。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-126">Most of the post-upgrade configuration for channels requires few manual steps.</span></span> <span data-ttu-id="3c6ab-127">顧客はアップグレード前およびアップグレード後のチェックリストを使用して、完了する必要があるタスクについて知ることができます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-127">Customers can then use the pre-upgrade and post-upgrade checklists to learn about the tasks that must be completed.</span></span> <span data-ttu-id="3c6ab-128">アップグレード後のタスクには、アップグレードされたデータベースから店舗への完全な同期の開始、アップグレードされたデータベースに対するチャンネル、レジスター、およびデバイスの検証、トランザクションの同期の検証、N-1サポートが実施されていることの検証が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-128">The post-upgrade tasks include initiating a full sync to the stores from the upgraded database, validating channels, registers, and devices against the upgraded database, validating transaction synchronization, and validating that N-1 support is in place.</span></span>
 
<span data-ttu-id="3c6ab-129">N-1 のサポートでは、顧客は Commerce 本部で N-1 パッケージをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-129">For N-1 support, the customer must install the N-1 package in Commerce headquarters.</span></span> <span data-ttu-id="3c6ab-130">店舗では設定は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-130">No setup is required in the stores.</span></span> <span data-ttu-id="3c6ab-131">このインストールは、N-1 関連の構成の完了後、アップグレード ウィンドウで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-131">This installation must be done during the upgrade window, after the N-1-related configuration has been completed.</span></span>

<span data-ttu-id="3c6ab-132">Commerce 本部のアップグレードと、N-1 の設定の完了後、N-1 店舗のコンポーネントが Commerce 本部と通信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-132">After the Commerce headquarters upgrade and N-1 setup are completed, the N-1 store components can communicate with Commerce headquarters.</span></span> <span data-ttu-id="3c6ab-133">N-1 のサポートのためにインストールが必要なチャネル側コンポーネントはありません。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-133">No channel-side components must be installed for N-1 support.</span></span> <span data-ttu-id="3c6ab-134">ただし、N-1 店舗が Commerce 本部と通信できるようにするためには、レジ担当者が最初にサイン インした際にパスワードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-134">However, to enable the N-1 store to communicate with Commerce headquarters, cashiers must change their password the first time that they sign in.</span></span>
 
<span data-ttu-id="3c6ab-135">N-1インストールの手順については、 [段階的なロールアウト (N-1) インストール、コンフィギュレーション、および切替ガイド](n-1-installation-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-135">For instructions for N-1 installation, see [Phased Rollout (N-1) installation, configuration, and cutover guide](n-1-installation-configuration.md).</span></span>
