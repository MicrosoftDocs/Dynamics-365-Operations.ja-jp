---
title: 配置の保守操作
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境の保守操作を実行する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: fc4696478af69226071b6d445258b781da786437
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096882"
---
# <a name="maintenance-operations-for-deployments"></a><span data-ttu-id="e1f9b-103">配置の保守操作</span><span class="sxs-lookup"><span data-stu-id="e1f9b-103">Maintenance operations for deployments</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="e1f9b-104">このトピックでは、[セルフサービス配置](infrastructure-stack.md) エクスペリエンスを使用して、配置された環境の保守操作を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-104">This topic explains how to perform maintenance operations for an environment that was deployed by using the [self-service deployment](infrastructure-stack.md) experience.</span></span>

## <a name="restart-services"></a><span data-ttu-id="e1f9b-105">サービスをリセット</span><span class="sxs-lookup"><span data-stu-id="e1f9b-105">Restart services</span></span>

<span data-ttu-id="e1f9b-106">サービスの再開機能を使用すると、Microsoft サブスクリプションで展開された階層 2、階層 3、階層 4、または階層 5 の標準承認テスト (サンドボックス) 環境に関連付けられた個々のサービスを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-106">You can use the restart services functionality to restart individual services that are associated with a Tier 2, Tier 3, Tier 4, or Tier 5 standard acceptance test (sandbox) environment that is deployed in a Microsoft subscription.</span></span> <span data-ttu-id="e1f9b-107">再起動できるサービスは、**AOS サービス**、**DIXF (データ インポート エキスポート フレームワーク サービス)**、および**MR (Management Reporter サービス)** です。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-107">The services that you can restart are **AOS service**, **DIXF (Data import export framework service)**, and **MR (Management Reporter service)**.</span></span>

<span data-ttu-id="e1f9b-108">サービスを再起動するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-108">To restart a service, follow these steps.</span></span>

1. <span data-ttu-id="e1f9b-109">Microsoft Dynamics Lifecycle Services (LCS) の環境の詳細ページで、**メンテナンス \> サービスの再起動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-109">In Microsoft Dynamics Lifecycle Services (LCS), on the environment details page, select **Maintain \> Restart service**.</span></span>
2. <span data-ttu-id="e1f9b-110">再起動するサービスを選択し、**確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-110">Select the service to restart, and then select **Confirm**.</span></span>

    <span data-ttu-id="e1f9b-111">再起動時、環境のステータスが**サービスの再起動中**に更新されます。その他のメンテナンス操作を開始することはできません。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-111">During the restart, the environment's status is updated to **Restarting service**, and you can't start any other maintenance operations.</span></span> <span data-ttu-id="e1f9b-112">環境のステータスは、サービスの再起動後に、**展開済み** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-112">After the service has been restarted, the environment's status is returned to **Deployed**.</span></span>

## <a name="maintenance-mode"></a><span data-ttu-id="e1f9b-113">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="e1f9b-113">Maintenance mode</span></span>

<span data-ttu-id="e1f9b-114">Finance and Operations アプリには、[メンテナンス モード](../sysadmin/maintenance-mode.md) という名前のシステム全体に適用される設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-114">Finance and Operations apps includes a system-wide setting that is named [maintenance mode](../sysadmin/maintenance-mode.md).</span></span> <span data-ttu-id="e1f9b-115">メンテナンス モードでは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-115">Maintenance mode gives system admins a safe way to make system changes that might affect system functionality.</span></span> <span data-ttu-id="e1f9b-116">たとえば、コンフィギュレーション キーは、オンまたはオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-116">For example, configuration keys can be turned on or off.</span></span> <span data-ttu-id="e1f9b-117">メンテナンス モードがオンのとき、システム管理者および**メンテナンス モード** ユーザー ロールが割り当てられたユーザーのみがシステムにサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-117">While maintenance mode is on, only the system admin and users who are assigned to the **Maintenance mode** user role can sign in to the system.</span></span> <span data-ttu-id="e1f9b-118">既定では、メンテナンス モードがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-118">By default, maintenance mode is turned off.</span></span>

<span data-ttu-id="e1f9b-119">メンテナンス モードのオン/オフを切り替えるには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-119">To turn maintenance mode on or off, follow these steps.</span></span>

1. <span data-ttu-id="e1f9b-120">LCS の環境の詳細ページで、**メンテナンス \> メンテナンス モードを有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-120">In LCS, on the environment details page, select **Maintain \> Enable Maintenance mode**.</span></span>

    <span data-ttu-id="e1f9b-121">環境の状態は、**配置済み**から**サービス中**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-121">The environment's status is changed from **Deployed** to **Servicing**.</span></span> <span data-ttu-id="e1f9b-122">メンテナンス モードがオンになると、環境のステータスが**メンテナンス中**に更新され、システム管理者のみがログインできます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-122">After maintenance mode has been turned on, the environment's status is updated to **In Maintenance**, and only the system admin can sign in.</span></span>

2. <span data-ttu-id="e1f9b-123">システム管理者が構成の変更を終了したら、環境の詳細ページで**メンテナンス \> メンテナンス モードを無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-123">After the system admin has finished making configuration changes, on the environment details page, select **Maintain \> Disable Maintenance mode**.</span></span>

    <span data-ttu-id="e1f9b-124">環境の状態は、**メンテナンス中**から**サービス中**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-124">The environment's status is changed from **In Maintenance** to **Servicing**.</span></span> <span data-ttu-id="e1f9b-125">環境のステータスは、メンテナンス モードがオフになると、**展開済み** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-125">After maintenance mode has been turned off, the environment's status is returned to **Deployed**.</span></span> <span data-ttu-id="e1f9b-126">環境の履歴が更新され、環境がメンテナンス モードに戻ったことが反映されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-126">The environment history is updated to reflect the fact that the environment was put into maintenance mode.</span></span>

## <a name="access-database"></a><span data-ttu-id="e1f9b-127">データベースへのアクセス</span><span class="sxs-lookup"><span data-stu-id="e1f9b-127">Access database</span></span>

<span data-ttu-id="e1f9b-128">[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置された環境では、リモート アクセスがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-128">Remote access is turned off for environments that were deployed by using the [self-service deployment](infrastructure-stack.md) experience.</span></span> <span data-ttu-id="e1f9b-129">実装時に、トラブルシューティング目的で階層 2、階層 3、階層 4、または階層 5 の標準受け入れテスト環境のデータベースに接続する必要がある場合、必要に応じてアクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-129">During implementation, if you must connect to the database on your Tier 2, Tier 3, Tier 4 or Tier 5 standard acceptance test environments for troubleshooting purposes, access will be granted as it's required.</span></span> <span data-ttu-id="e1f9b-130">アクセス権は永続的ではありません。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-130">The access won't be persistent.</span></span>

<span data-ttu-id="e1f9b-131">データベースに接続するには、以下の手順をします。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-131">To connect to a database, follow these steps.</span></span>

1. <span data-ttu-id="e1f9b-132">LCS でデータベース資格情報を参照するアクセスを要求します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-132">Request access to view the database credentials in LCS.</span></span> <span data-ttu-id="e1f9b-133">環境の詳細ページの**アクセスの理由を**フィールドで、アクセスを要求する理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-133">On the environment details page, in the **Reason for access** field, select your reason for requesting access.</span></span> <span data-ttu-id="e1f9b-134">**詳細**フィールドに、その他の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-134">In the **Details** field, enter any additional details.</span></span> 
2. <span data-ttu-id="e1f9b-135">**アクセス権の要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-135">Select **Request access**.</span></span>

    <span data-ttu-id="e1f9b-136">ユーザー固有の資格情報を作成する要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-136">A request to create user-specific credentials is submitted.</span></span> <span data-ttu-id="e1f9b-137">要求は送信するとすぐに自動的に承認されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-137">The request is automatically approved as soon as you submit it.</span></span> <span data-ttu-id="e1f9b-138">8 時間の有効期限があります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-138">It has an expiration time of eight hours.</span></span> <span data-ttu-id="e1f9b-139">数分以内に、LCS 環境の詳細ページでデータベース資格情報を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-139">In a few minutes, you will be able to view the database credentials on the environment details page in LCS.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e1f9b-140">データベース資格情報は、8 時間有効です。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-140">The database credentials are valid for eight hours.</span></span> <span data-ttu-id="e1f9b-141">8 時間後、資格情報の期限が切れたら、もう一度アクセス権を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-141">After eight hours, the credentials expire, and you must request access again.</span></span>

3. <span data-ttu-id="e1f9b-142">接続文字列とアクセスの詳細を表示するために環境の詳細ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-142">Refresh the environment details page to view the connection string and access details.</span></span>

    <span data-ttu-id="e1f9b-143">自分に付与されるアクセス許可は、**アクセスの理由を**フィールドで選択した理由によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-143">The access that is granted to you depends on the reason that you selected in the **Reason for access** field.</span></span> <span data-ttu-id="e1f9b-144">たとえば、理由として**AX トラブルシューティング**を選択した場合、AX データベースへの読み取り専用アクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-144">For example, if you selected **AX troubleshooting** as the reason, read-only access to the AX database is granted.</span></span> <span data-ttu-id="e1f9b-145">**パフォーマンスのチューニング**を理由として選択した場合、AX データベースへの書き込みアクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-145">If you selected **Performance tuning** as the reason, write access to the AX database is granted.</span></span>

4. <span data-ttu-id="e1f9b-146">LCS を通じて Microsoft Azure SQL データベースにアクセスするには、Microsoft SQL Server Management Studio を使用して SQL データベースに接続するコンピューターの IP アドレスが承認済みリスト (「ホワイトリスト」とも呼ばれます) に追加されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-146">Before you can access Microsoft Azure SQL Database through LCS, the IP address of the computer where you will use Microsoft SQL Server Management Studio to connect to the SQL database must be added to the approved list (sometimes referred to as the "whitelist").</span></span>

    <span data-ttu-id="e1f9b-147">この手順を完了するには、新しい SQL データベース ファイアウォール ルールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-147">To complete this step, you can add a new SQL Database firewall rule:</span></span>

    1. <span data-ttu-id="e1f9b-148">LCS の環境の詳細ページで、**メンテナンス \> アクセスを有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-148">In LCS, on the environment details page, select **Maintain \> Enable access**.</span></span>
    2. <span data-ttu-id="e1f9b-149">新しいルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-149">Add a new rule.</span></span> <span data-ttu-id="e1f9b-150">**サービス**フィールドで、**Azure SQL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-150">In the **Service** field, select **Azure SQL**.</span></span>
    3. <span data-ttu-id="e1f9b-151">ルールの名前を入力し、コンピューターの IP アドレスを入力し、**確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-151">Enter a name for the rule, enter the IP address of the computer, and then select **Confirm**.</span></span>

    <span data-ttu-id="e1f9b-152">このルールにも、8 時間の有効期限があります。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-152">This rule also has an expiration time of eight hours.</span></span>

5. <span data-ttu-id="e1f9b-153">承認済リストに追加されているコンピューターで、Management Studio を開き、接続の詳細を使用して必要なデータベースに接続します。</span><span class="sxs-lookup"><span data-stu-id="e1f9b-153">On the computer that has been added to the approved list, open Management Studio, and use the connection details to connect to the required database.</span></span>
