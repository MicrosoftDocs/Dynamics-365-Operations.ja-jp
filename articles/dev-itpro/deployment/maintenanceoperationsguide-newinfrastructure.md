---
title: 配置の保守操作
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境の保守操作を実行する方法について説明します。
author: manado
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 55762be3e3481f1daa71c852a40657e0c8b05c1e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368625"
---
# <a name="maintenance-operations-for-deployments"></a><span data-ttu-id="92e52-103">配置の保守操作</span><span class="sxs-lookup"><span data-stu-id="92e52-103">Maintenance operations for deployments</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="92e52-104">このドキュメントでは、「[セルフ サービス配置](infrastructure-stack.md)」エクスペリエンスを使用して配置された Dynamics 365 for Finance and Operations 環境の保守操作を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="92e52-104">This document explains how to perform maintenance operations for a Dynamics 365 for Finance and Operations environment deployed using the [self-service deployment](infrastructure-stack.md) experience.</span></span>

## <a name="restart-services"></a><span data-ttu-id="92e52-105">サービスをリセット</span><span class="sxs-lookup"><span data-stu-id="92e52-105">Restart services</span></span>
<span data-ttu-id="92e52-106">サービスの再開機能を使用すると、Microsoft サブスクリプションで展開された階層 2、階層 3、階層 4、または階層 5 の標準承認テスト (サンドボックス) 環境に関連付けられた個々のサービスを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="92e52-106">You can use the restart services functionality to restart individual services that are associated with a Tier 2, Tier 3, Tier 4, or Tier 5 standard acceptance test (sandbox) environment that is deployed in a Microsoft subscription.</span></span>

<span data-ttu-id="92e52-107">サービスを再起動するには、サポート チケットを作成し、次の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="92e52-107">To restart a service, create a support ticket and provide the following details:</span></span>

- <span data-ttu-id="92e52-108">**プロジェクト ID**: LCS プロジェクトの ID。</span><span class="sxs-lookup"><span data-stu-id="92e52-108">**Project ID**: ID of the LCS project.</span></span>
- <span data-ttu-id="92e52-109">**環境 ID**: 環境の URL にある GUID (環境 ID)。</span><span class="sxs-lookup"><span data-stu-id="92e52-109">**Environment ID**: GUID available in the URL (EnvironmentID) for the environment.</span></span>
- <span data-ttu-id="92e52-110">**再起動するサービス**: AOS、DIXF、MR、バッチ。</span><span class="sxs-lookup"><span data-stu-id="92e52-110">**Service to restart**: AOS, DIXF, MR, Batch.</span></span>
- <span data-ttu-id="92e52-111">**ダウンタイム開始**: 協定世界時 (UTC) でダウンタイム開始を指定します。</span><span class="sxs-lookup"><span data-stu-id="92e52-111">**Downtime start**: Provide a start downtime in Universal Time Coordinated (UTC).</span></span>
- <span data-ttu-id="92e52-112">**ダウンタイム終了**: UTC でダウンタイム終了を指定します。</span><span class="sxs-lookup"><span data-stu-id="92e52-112">**Downtime end**: Provide an end downtime in UTC.</span></span>

> [!NOTE]
> <span data-ttu-id="92e52-113">この機能は、2019 年早期に Lifecycle Services (LCS) を通じたセルフ サービスになります。</span><span class="sxs-lookup"><span data-stu-id="92e52-113">This functionality will be self-service through Lifecycle Services (LCS) in early 2019.</span></span>

## <a name="maintenance-mode"></a><span data-ttu-id="92e52-114">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="92e52-114">Maintenance mode</span></span>
<span data-ttu-id="92e52-115">Finance and Operations には、[メンテナンス モード](../sysadmin/maintenance-mode.md)という名前のシステム全体に適用される設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="92e52-115">Finance and Operations includes a system-wide setting that is named [Maintenance mode](../sysadmin/maintenance-mode.md).</span></span> <span data-ttu-id="92e52-116">メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="92e52-116">When maintenance mode is turned on, it provides a safe way for system administrators to make system changes that might affect system functionality.</span></span> <span data-ttu-id="92e52-117">たとえば、コンフィギュレーション キーは、有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="92e52-117">For example, configuration keys can be enabled or disabled.</span></span> <span data-ttu-id="92e52-118">メンテナンス モードがオンのとき、システム管理者およびメンテナンス モード ユーザー ロールが割り当てられたユーザーのみがシステムにサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="92e52-118">While maintenance mode is on, only system administrators and users assigned to the Maintenance mode user role can sign in to the system.</span></span> <span data-ttu-id="92e52-119">既定では、メンテナンス モードがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="92e52-119">By default, maintenance mode is turned off.</span></span>

<span data-ttu-id="92e52-120">メンテナンス モードを有効/無効にするには、サポート チケットを作成し、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="92e52-120">To enable/disable maintenance mode, create a support ticket and provide the following details:</span></span>

- <span data-ttu-id="92e52-121">**プロジェクト ID**: LCS プロジェクトの ID。</span><span class="sxs-lookup"><span data-stu-id="92e52-121">**Project ID**: ID of the LCS project.</span></span>
- <span data-ttu-id="92e52-122">**環境 ID**: 環境の URL にある GUID (環境 ID)。</span><span class="sxs-lookup"><span data-stu-id="92e52-122">**Environment ID**: GUID available in the URL (EnvironmentID) for the environment.</span></span>
- <span data-ttu-id="92e52-123">**メンテナンス モードを有効化する開始時刻**: メンテナンス モードを有効にする開始時刻を UTC で指定します。</span><span class="sxs-lookup"><span data-stu-id="92e52-123">**Start time for enabling maintenance mode**: Provide a start time in UTC for when you want to enable maintenance mode.</span></span>
- <span data-ttu-id="92e52-124">**メンテナンス モードを無効化する開始時刻**: メンテナンス モードを無効にする開始時刻を UTC で指定します。</span><span class="sxs-lookup"><span data-stu-id="92e52-124">**Start time for disabling maintenance mode**: Provide a start time in UTC for when you want to disable maintenance mode.</span></span>

> [!NOTE]
> <span data-ttu-id="92e52-125">この機能は、2019 年早期に Lifecycle Services (LCS) を通じたセルフ サービスになります。</span><span class="sxs-lookup"><span data-stu-id="92e52-125">This functionality will be self-service through Lifecycle Services (LCS) in early 2019.</span></span>

## <a name="access-database"></a><span data-ttu-id="92e52-126">データベースへのアクセス</span><span class="sxs-lookup"><span data-stu-id="92e52-126">Access database</span></span>
<span data-ttu-id="92e52-127">[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置された環境では、リモート デスクトップ アクセスがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="92e52-127">Environments deployed using the [self-service deployment](infrastructure-stack.md) experience have Remote Desktop Access turned off.</span></span> <span data-ttu-id="92e52-128">Finance and Operations の実装の一環として、トラブルシューティングのために標準受け入れテスト環境でデータベースに接続する必要がある場合、サポート チケットを作成し、次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="92e52-128">As part of implementing Finance and Operations, if you need to connect to the database on your Standard Acceptance Test environments for troubleshooting, create a support ticket and provide the following details:</span></span>

- <span data-ttu-id="92e52-129">**プロジェクト ID**: LCS プロジェクトの ID。</span><span class="sxs-lookup"><span data-stu-id="92e52-129">**Project ID**: ID of the LCS project.</span></span>
- <span data-ttu-id="92e52-130">**環境 ID**: 環境の URL にある GUID (環境 ID)。</span><span class="sxs-lookup"><span data-stu-id="92e52-130">**Environment ID**: GUID available in the URL (EnvironmentID) for the environment.</span></span>
- <span data-ttu-id="92e52-131">**実行する必要があるクエリ**: 実行するクエリです。</span><span class="sxs-lookup"><span data-stu-id="92e52-131">**Query that needs to be executed**: Query that you want to execute.</span></span>

> [!NOTE]
> <span data-ttu-id="92e52-132">この機能は、2019 年早期に Lifecycle Services (LCS) を通じたセルフ サービスになります。</span><span class="sxs-lookup"><span data-stu-id="92e52-132">This functionality will be self-service through Lifecycle Services (LCS) in early 2019.</span></span> <span data-ttu-id="92e52-133">Azure SQL データベースへのアクセスは永続的ではありません。ただし、Lifecycle Services 環境の詳細ページを使用して直接データベースへのアクセスを要求することができます。</span><span class="sxs-lookup"><span data-stu-id="92e52-133">The access to the Azure SQL database will not be persistent; however, you can request access to the database directly through the Lifecycle Services environment details page.</span></span>   <span data-ttu-id="92e52-134">アクセスを取得するプロセスは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="92e52-134">The process of getting access will be as follows:</span></span>
>- <span data-ttu-id="92e52-135">SQL Management Studio を使用して Azure SQL データベースに接続するために使用するコンピューターの IP アドレスをホワイトリストに追加することで、LCS を通じて Azure SQL へのアクセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="92e52-135">Enable access to Azure SQL through LCS by whitelisting the IP address of the machine that you will use to connect to the Azure SQL database using SQL Management Studio.</span></span> 
>- <span data-ttu-id="92e52-136">その後、アクセスを要求する理由を入力することにより、アクセスを要求して LCS を通じてデータベースの資格情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="92e52-136">After this is done, you can request access to see the database credentials through LCS by entering a reason for requesting access.</span></span> 
>- <span data-ttu-id="92e52-137">要求を送信するとすぐに**自動承認**されます。</span><span class="sxs-lookup"><span data-stu-id="92e52-137">As soon as you submit the request, it gets **auto-approved**.</span></span> <span data-ttu-id="92e52-138">数分以内に LCS 環境の詳細ページでデータベース アクセスの資格情報を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="92e52-138">You will be able to see the database access credentials within a few minutes, on the LCS environment details page.</span></span> 
>- <span data-ttu-id="92e52-139">資格情報は 8 時間有効であり、その期間の後に有効期限が切れることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="92e52-139">Note that the credentials are valid for 8 hours and will expire after that duration.</span></span> <span data-ttu-id="92e52-140">8 時間の後、アクセス権が有効期限切れになり、もう一度アクセス権を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92e52-140">After 8 hours the access expires and you will need to request access again.</span></span> 
> <span data-ttu-id="92e52-141">上記の手順を実行する方法の詳細については、この機能が 1 月に Lifecycle Services から利用可能になるとすぐに公開されます。</span><span class="sxs-lookup"><span data-stu-id="92e52-141">Additional information on how to perform the above steps  will be published as soon as this feature is made available in January, through Lifecycle Services.</span></span>

