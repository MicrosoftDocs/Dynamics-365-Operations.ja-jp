---
title: 配置の保守操作
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境の保守操作を実行する方法について説明します。
author: laneswenka
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6f52269bd694d6900640e890fd57a84ca3fbe853
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745647"
---
# <a name="maintenance-operations-for-deployments"></a><span data-ttu-id="b9036-103">配置の保守操作</span><span class="sxs-lookup"><span data-stu-id="b9036-103">Maintenance operations for deployments</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="b9036-104">このトピックでは、[セルフサービス配置](infrastructure-stack.md) エクスペリエンスを使用して、配置された環境の保守操作を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b9036-104">This topic explains how to perform maintenance operations for an environment that was deployed by using the [self-service deployment](infrastructure-stack.md) experience.</span></span>

## <a name="restart-services"></a><span data-ttu-id="b9036-105">サービスをリセット</span><span class="sxs-lookup"><span data-stu-id="b9036-105">Restart services</span></span>

<span data-ttu-id="b9036-106">サービスの再開機能を使用すると、Microsoft サブスクリプションで展開された階層 2、階層 3、階層 4、または階層 5 の標準承認テスト (サンドボックス) 環境に関連付けられた個々のサービスを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="b9036-106">You can use the restart services functionality to restart individual services that are associated with a Tier 2, Tier 3, Tier 4, or Tier 5 standard acceptance test (sandbox) environment that is deployed in a Microsoft subscription.</span></span> <span data-ttu-id="b9036-107">再起動できるサービスは、**AOS サービス**、**DIXF (データ インポート エキスポート フレームワーク サービス)**、および **MR (Management Reporter サービス)** です。</span><span class="sxs-lookup"><span data-stu-id="b9036-107">The services that you can restart are **AOS service**, **DIXF (Data import export framework service)**, and **MR (Management Reporter service)**.</span></span>

<span data-ttu-id="b9036-108">サービスを再起動するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9036-108">To restart a service, follow these steps.</span></span>

1. <span data-ttu-id="b9036-109">Microsoft Dynamics Lifecycle Services (LCS) の環境の詳細ページで、**メンテナンス \> サービスの再起動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9036-109">In Microsoft Dynamics Lifecycle Services (LCS), on the environment details page, select **Maintain \> Restart service**.</span></span>
2. <span data-ttu-id="b9036-110">再起動するサービスを選択し、**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9036-110">Select the service to restart, and then select **Confirm**.</span></span>

    <span data-ttu-id="b9036-111">再起動時、環境のステータスが **サービスの再起動中** に更新されます。その他のメンテナンス操作を開始することはできません。</span><span class="sxs-lookup"><span data-stu-id="b9036-111">During the restart, the environment's status is updated to **Restarting service**, and you can't start any other maintenance operations.</span></span> <span data-ttu-id="b9036-112">環境のステータスは、サービスの再起動後に、**展開済み** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="b9036-112">After the service has been restarted, the environment's status is returned to **Deployed**.</span></span>

## <a name="maintenance-mode"></a><span data-ttu-id="b9036-113">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="b9036-113">Maintenance mode</span></span>

<span data-ttu-id="b9036-114">Finance and Operations アプリには、[メンテナンス モード](../sysadmin/maintenance-mode.md) という名前のシステム全体に適用される設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9036-114">Finance and Operations apps includes a system-wide setting that is named [maintenance mode](../sysadmin/maintenance-mode.md).</span></span> <span data-ttu-id="b9036-115">メンテナンス モードでは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="b9036-115">Maintenance mode gives system admins a safe way to make system changes that might affect system functionality.</span></span> <span data-ttu-id="b9036-116">たとえば、コンフィギュレーション キーは、オンまたはオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9036-116">For example, configuration keys can be turned on or off.</span></span> <span data-ttu-id="b9036-117">メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード** ユーザー ロールが割り当てられたユーザーのみがシステムにサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9036-117">While maintenance mode is on, only the system admin and users who are assigned to the **Maintenance mode** user role can sign in to the system.</span></span> <span data-ttu-id="b9036-118">既定では、メンテナンス モードがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="b9036-118">By default, maintenance mode is turned off.</span></span>

<span data-ttu-id="b9036-119">メンテナンス モードのオン/オフを切り替えるには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9036-119">To turn maintenance mode on or off, follow these steps.</span></span>

1. <span data-ttu-id="b9036-120">LCS の環境の詳細ページで、**メンテナンス \> メンテナンス モードを有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9036-120">In LCS, on the environment details page, select **Maintain \> Enable Maintenance mode**.</span></span>

    <span data-ttu-id="b9036-121">環境の状態は、**配置済み** から **サービス中** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="b9036-121">The environment's status is changed from **Deployed** to **Servicing**.</span></span> <span data-ttu-id="b9036-122">メンテナンス モードがオンになると、環境のステータスが **メンテナンス中** に更新され、システム管理者のみがログインできます。</span><span class="sxs-lookup"><span data-stu-id="b9036-122">After maintenance mode has been turned on, the environment's status is updated to **In Maintenance**, and only the system admin can sign in.</span></span>

2. <span data-ttu-id="b9036-123">システム管理者が構成の変更を終了したら、環境の詳細ページで **メンテナンス \> メンテナンス モードを無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9036-123">After the system admin has finished making configuration changes, on the environment details page, select **Maintain \> Disable Maintenance mode**.</span></span>

    <span data-ttu-id="b9036-124">環境の状態は、**メンテナンス中** から **サービス中** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="b9036-124">The environment's status is changed from **In Maintenance** to **Servicing**.</span></span> <span data-ttu-id="b9036-125">環境のステータスは、メンテナンス モードがオフになると、**展開済み** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="b9036-125">After maintenance mode has been turned off, the environment's status is returned to **Deployed**.</span></span> <span data-ttu-id="b9036-126">環境の履歴が更新され、環境がメンテナンス モードに戻ったことが反映されます。</span><span class="sxs-lookup"><span data-stu-id="b9036-126">The environment history is updated to reflect the fact that the environment was put into maintenance mode.</span></span>

## <a name="access-database"></a><span data-ttu-id="b9036-127">データベースへのアクセス</span><span class="sxs-lookup"><span data-stu-id="b9036-127">Access database</span></span>

<span data-ttu-id="b9036-128">[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置された環境では、リモート アクセスがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="b9036-128">Remote access is turned off for environments that were deployed by using the [self-service deployment](infrastructure-stack.md) experience.</span></span> <span data-ttu-id="b9036-129">実装時に、トラブルシューティング目的で階層 2、階層 3、階層 4、または階層 5 の標準受け入れテスト環境のデータベースに接続する必要がある場合、必要に応じてアクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="b9036-129">During implementation, if you must connect to the database on your Tier 2, Tier 3, Tier 4 or Tier 5 standard acceptance test environments for troubleshooting purposes, access will be granted as it's required.</span></span> <span data-ttu-id="b9036-130">アクセス権は永続的ではありません。</span><span class="sxs-lookup"><span data-stu-id="b9036-130">The access won't be persistent.</span></span>

<span data-ttu-id="b9036-131">データベースに接続するには、[Just-In-Time のアクセスを有効にする](../database/database-just-in-time-jit-access.md)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b9036-131">To connect to a database, follow the instructions in [Enable just-in-time access](../database/database-just-in-time-jit-access.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]