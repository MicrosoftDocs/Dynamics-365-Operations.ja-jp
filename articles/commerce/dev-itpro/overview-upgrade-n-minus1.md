---
title: Commerce のアップグレードおよび N-1 のサポート
description: Dynamics 365 Commerce のリリースで、アップグレードと N-1 サポートが有効になりました。
author: athinesh99
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.custom: 44351
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2017-07-31
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: dc54586f85ec9d06b3720441233eca0a02a52a8e
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937140"
---
# <a name="upgrade-and-n-1-support-for-commerce"></a><span data-ttu-id="63764-103">Commerce のアップグレードおよび N-1 のサポート</span><span class="sxs-lookup"><span data-stu-id="63764-103">Upgrade and N-1 support for Commerce</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63764-104">Microsoft Dynamics 365 Retail の 2017 年 7 月のリリースで、アップグレードと N-1 サポートが有効になりました。</span><span class="sxs-lookup"><span data-stu-id="63764-104">Upgrade and N-1 support have been enabled in the July 2017 release of Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="63764-105">N-1 のサポートによって、Microsoft Dynamics AX 2012 R3 累積更新プログラム 10 (CU10) を実行する店舗を持つ顧客は、アップグレード後にバックオフィスで作業できます。</span><span class="sxs-lookup"><span data-stu-id="63764-105">N-1 support lets customers who have stores that run Microsoft Dynamics AX 2012 R3 Cumulative Update 10 (CU10) work with Headquarters after an upgrade.</span></span> <span data-ttu-id="63764-106">アップグレードと N-1 サポートの主な目的は、AX 2012 R3 の顧客がクラウドの利点を活用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="63764-106">The main purpose of upgrade and N-1 support is to let AX 2012 R3 customers take advantage of the benefits of the cloud.</span></span>

<span data-ttu-id="63764-107">次の機能を使用すると、顧客はシームレスにアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="63764-107">The following features let customers upgrade in a seamless manner:</span></span>

- <span data-ttu-id="63764-108">アップグレード プロセスを通じて、AX 2012 R3 からバックオフィスへのデータベース アップグレードを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="63764-108">Users can now perform database upgrade from AX 2012 R3 to Headquarters through the upgrade process.</span></span>
- <span data-ttu-id="63764-109">AX 2012 R3 CU10 のコンポーネントを使用して店舗を運営することができます。</span><span class="sxs-lookup"><span data-stu-id="63764-109">Users can operate their stores by using the components of AX 2012 R3 CU10.</span></span>
- <span data-ttu-id="63764-110">アップグレード前とアップグレード後のチェックリストの検証は、アップグレード プロセスに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="63764-110">Pre-upgrade and post-upgrade checklist validations are built into the upgrade process.</span></span>
- <span data-ttu-id="63764-111">アップグレード プロセスでは、エラー処理とメッセージングが強化されているため、顧客は問題を迅速にデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="63764-111">The upgrade process has enhanced error handling and messaging, so that customers can quickly debug issues.</span></span>
- <span data-ttu-id="63764-112">ユーザーは、ツールを使用して、既存のバックオフィスのカスタムの X++ コードを、そのバックオフィスのアップグレードされたバージョンに移行することができます。</span><span class="sxs-lookup"><span data-stu-id="63764-112">Users can use tools to bring forward custom X++ code in their existing Headquarters to the upgraded version of the headquarters.</span></span>

<span data-ttu-id="63764-113">アップグレード手順は、Retail を最新バージョンにアップグレードする手順とほぼ同じです。</span><span class="sxs-lookup"><span data-stu-id="63764-113">The upgrade procedure is largely the same as the procedure for upgrading Retail to the latest version.</span></span> <span data-ttu-id="63764-114">一般に、アップグレードに関する詳細については、「[AX 2012 から Dynamics 365 Retail へのアップグレードの概要](../../fin-ops-core/dev-itpro/migration-upgrade/upgrade-overview-2012.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63764-114">For details about upgrade in general, see [Upgrade overview: AX 2012 to Dynamics 365 Retail](../../fin-ops-core/dev-itpro/migration-upgrade/upgrade-overview-2012.md).</span></span>

<span data-ttu-id="63764-115">計画的なダウンタイムが必要です。</span><span class="sxs-lookup"><span data-stu-id="63764-115">Planned downtime is required.</span></span> <span data-ttu-id="63764-116">アップグレード分析を最初に行います。</span><span class="sxs-lookup"><span data-stu-id="63764-116">Upgrade analysis is done first.</span></span> <span data-ttu-id="63764-117">アップグレード分析は、Microsoft Dynamics AX 2012 データベースに対して実行され、Microsoft Dynamics Lifecycle Services (LCS) 診断サービスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="63764-117">The upgrade analysis runs against the Microsoft Dynamics AX 2012 database and is based on the Microsoft Dynamics Lifecycle Services (LCS) Diagnostic service.</span></span> <span data-ttu-id="63764-118">このステップでは、アップグレードをより迅速かつ低コストで行うための作業を特定します。</span><span class="sxs-lookup"><span data-stu-id="63764-118">This step identifies tasks that can help make upgrade faster and less expensive.</span></span> <span data-ttu-id="63764-119">また、必要な SQL 構成、データ バックオフィス クリーンアップ、推奨されない機能を識別します。</span><span class="sxs-lookup"><span data-stu-id="63764-119">It also identifies the required SQL configuration, data headquarters cleanup, and deprecated features.</span></span>
  
<span data-ttu-id="63764-120">その後、実際のデータ アップグレード プロセスが発生します。</span><span class="sxs-lookup"><span data-stu-id="63764-120">The actual data upgrade process then occurs.</span></span> <span data-ttu-id="63764-121">AX 2012 データベースは、Microsoft Azure SQL データベースに移動され、データ アップグレード パッケージは runbook プロセスを通じて通常どおり実行されます。</span><span class="sxs-lookup"><span data-stu-id="63764-121">The AX 2012 database is moved to Microsoft Azure SQL Database, and then the data upgrade package is run as usual, through the runbook process.</span></span> <span data-ttu-id="63764-122">アップグレードの検証が完了します。</span><span class="sxs-lookup"><span data-stu-id="63764-122">Upgrade validation is then done.</span></span> <span data-ttu-id="63764-123">検証ツールは、使用される前にアップグレードされた環境に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="63764-123">A validation tool is run against the upgraded environment before it's used.</span></span> <span data-ttu-id="63764-124">このツールは自動スモーク テストを実行して、サービスが動作してアクセス可能なこと、行数の一致、財務と在庫の調整などを検証します。</span><span class="sxs-lookup"><span data-stu-id="63764-124">This tool does an automated smoke test to verify that the service is running and accessible, row counts match, financials and inventory reconcile, and so on.</span></span>

<span data-ttu-id="63764-125">チャネルのアップグレード後構成のほとんどにおいて、手動での手順をほぼ必要としません。</span><span class="sxs-lookup"><span data-stu-id="63764-125">Most of the post-upgrade configuration for channels requires few manual steps.</span></span> <span data-ttu-id="63764-126">顧客はアップグレード前およびアップグレード後のチェックリストを使用して、完了する必要があるタスクについて知ることができます。</span><span class="sxs-lookup"><span data-stu-id="63764-126">Customers can then use the pre-upgrade and post-upgrade checklists to learn about the tasks that must be completed.</span></span> <span data-ttu-id="63764-127">アップグレード後のタスクには、アップグレードされたデータベースから店舗への完全な同期の開始、アップグレードされたデータベースに対するチャンネル、レジスター、およびデバイスの検証、トランザクションの同期の検証、N-1サポートが実施されていることの検証が含まれます。</span><span class="sxs-lookup"><span data-stu-id="63764-127">The post-upgrade tasks include initiating a full sync to the stores from the upgraded database, validating channels, registers, and devices against the upgraded database, validating transaction synchronization, and validating that N-1 support is in place.</span></span>

<span data-ttu-id="63764-128">N-1 のサポートでは、顧客は Commerce 本部で N-1 パッケージをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="63764-128">For N-1 support, the customer must install the N-1 package in Commerce headquarters.</span></span> <span data-ttu-id="63764-129">店舗では設定は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="63764-129">No setup is required in the stores.</span></span> <span data-ttu-id="63764-130">このインストールは、N-1 関連の構成の完了後、アップグレード ウィンドウで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63764-130">This installation must be done during the upgrade window, after the N-1-related configuration has been completed.</span></span>

<span data-ttu-id="63764-131">Commerce 本部のアップグレードと、N-1 の設定の完了後、N-1 店舗のコンポーネントが Commerce 本部と通信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="63764-131">After the Commerce headquarters upgrade and N-1 setup are completed, the N-1 store components can communicate with Commerce headquarters.</span></span> <span data-ttu-id="63764-132">N-1 のサポートのためにインストールが必要なチャネル側コンポーネントはありません。</span><span class="sxs-lookup"><span data-stu-id="63764-132">No channel-side components must be installed for N-1 support.</span></span> <span data-ttu-id="63764-133">ただし、N-1 店舗が Commerce 本部と通信できるようにするためには、レジ担当者が最初にサイン インした際にパスワードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63764-133">However, to enable the N-1 store to communicate with Commerce headquarters, cashiers must change their password the first time that they sign in.</span></span>

<span data-ttu-id="63764-134">N-1インストールの手順については、 [段階的なロールアウト (N-1) インストール、コンフィギュレーション、および切替ガイド](n-1-installation-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63764-134">For instructions for N-1 installation, see [Phased Rollout (N-1) installation, configuration, and cutover guide](n-1-installation-configuration.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]