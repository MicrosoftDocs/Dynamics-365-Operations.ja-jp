---
title: "サンドボックス データベース更新の要求"
description: "このトピックでは、サンドボックスのユーザー受け入れテスト (UAT) 環境で、Microsoft Dynamics 365 for Finance and Operations のデータベースの更新を要求する方法について説明します。"
author: Robadawy
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 257614
ms.assetid: 558598db-937e-4bfe-80c7-a861be021db1
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: de68ce0f8997fb73f8bff2681d58ddc0e833ca01
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="request-sandbox-database-refreshes"></a><span data-ttu-id="3bfbb-103">サンドボックス データベース更新の要求</span><span class="sxs-lookup"><span data-stu-id="3bfbb-103">Request sandbox database refreshes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bfbb-104">Microsoft Dynamics Lifecycle Services (LCS) を使用して、サンドボックス ユーザー承認テスト (UAT) 環境で、Microsoft Dynamics 365 for Finance and Operations のデータベースのリフレッシュを要求することができます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to request a refresh of the database for Microsoft Dynamics 365 for Finance and Operations, in a sandbox user acceptance testing (UAT) environment.</span></span> <span data-ttu-id="3bfbb-105">データベースの更新対象となるサンド ボックス UAT 環境に、本番環境のデータベース (および財務報告データベース) をコピーできます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-105">A database refresh lets you copy the database of your production environment (and the Financial Reporting database) into the target sandbox UAT environment.</span></span> <span data-ttu-id="3bfbb-106">別の UAT 環境を使用する場合は、その環境からデータベースをコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-106">If you have another UAT environment, you can also copy the databases from that environment.</span></span>

<span data-ttu-id="3bfbb-107">この機能により、生産データを使用して UAT 環境で予定されているコード変更をテストできます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-107">This functionality lets you use production data to test upcoming code changes in a UAT environment.</span></span> <span data-ttu-id="3bfbb-108">また、デバッグの目的で、生産データベースを UAT 環境にコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-108">You can also copy a production database into a UAT environment for debugging purposes.</span></span>

## <a name="database-refresh-process"></a><span data-ttu-id="3bfbb-109">データベース更新プロセス</span><span class="sxs-lookup"><span data-stu-id="3bfbb-109">Database refresh process</span></span>

<span data-ttu-id="3bfbb-110">Microsoft サービス エンジニアリング チームは、環境をオフラインにして、更新を実行し、環境をオンラインに戻します。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-110">The Microsoft Service Engineering team will take your environment offline, complete the refresh, and then bring the environment back online.</span></span> <span data-ttu-id="3bfbb-111">ダウンタイム期間が約 2 時間であると予測することができます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-111">You can expect the downtime period to be approximately two hours.</span></span> <span data-ttu-id="3bfbb-112">ユーザーが要求を入力してから、マイクロソフトのサービス エンジニアが措置を講じるまでの時間が、ユーザーの環境のダウンタイムよりも長くなります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-112">The period after you enter your request and before our Service Engineers take action will be longer than your environment's downtime.</span></span> <span data-ttu-id="3bfbb-113">今後、データベース更新を実行するために使用できるセルフ サービスのメソッドを提供する予定です。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-113">In the future, we will provide a self-service method that you can use to perform your database refreshes.</span></span>

1. <span data-ttu-id="3bfbb-114">LCS で、左上のハンバーガー アイコンを選択してから、**作業項目**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-114">In LCS, select the hamburger icon in the upper left, and then select **Work items**.</span></span>
2. <span data-ttu-id="3bfbb-115">**作業項目**ページの、ツールバーで**追加**を選択し、**データベースの更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-115">On the **Work items** page, select **Add** on the toolbar, and then select **Database refresh**.</span></span>
3. <span data-ttu-id="3bfbb-116">**データベース更新の要求**ダイアログ ボックスで、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-116">In the **Request for database refresh** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="3bfbb-117">**環境名**フィールドで、更新する環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-117">In the **Environment name** field, select the environment to refresh.</span></span>
    2. <span data-ttu-id="3bfbb-118">**データベース** フィールドでは、更新するデータベースは常に Microsoft Dynamics AX データベースまたは Finance and Operations データベースです。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-118">In the **Database** field, the database to refresh is always the Microsoft Dynamics AX database or the Finance and Operations database.</span></span> <span data-ttu-id="3bfbb-119">エンティティ格納などの他のデータベースでは、データベースの更新が現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-119">Other databases, such as Entity store aren't currently supported for database refresh.</span></span>
    3. <span data-ttu-id="3bfbb-120">チェック ボックスを隣に置いたステートメントを注意深く読んで確認してください。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-120">Carefully read and acknowledge the statements that have check boxes next to them.</span></span>

4. <span data-ttu-id="3bfbb-121">要求を送信した後、作業項目のリストに戻ります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-121">After you submit your request, you are returned to the list of work items.</span></span> <span data-ttu-id="3bfbb-122">ここで、要求のステータスを表示し、または再スケジューリングし、または要求をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-122">Here, you can view the status of the request, or reschedule or cancel the request.</span></span>
5. <span data-ttu-id="3bfbb-123">サービス エンジニア リング チームがお客様の要求を達成できることを確認したとき、その要求のステータスは **要求受入済** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-123">When the Service Engineering team has acknowledged that it can complete your request, the status of the request is changed to **Request accepted**.</span></span> <span data-ttu-id="3bfbb-124">この時点で、次のいずれかの手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-124">At this point, you can follow any of these steps:</span></span>

    - <span data-ttu-id="3bfbb-125">サービス エンジニア リング チームによる更新が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-125">Wait for the Service Engineering team to complete the refresh.</span></span> <span data-ttu-id="3bfbb-126">復元が完了したら、ステータスが **"成功"** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-126">When the restore is completed, the status is changed to **Succeeded**.</span></span>
    - <span data-ttu-id="3bfbb-127">ID を選択するか、要求を選択してツール バーで **再スケジューリング** を選択することにより、リクエストを再スケジューリングします。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-127">Reschedule the request by selecting the ID, or by selecting the request and then selecting **Reschedule** on the toolbar.</span></span> <span data-ttu-id="3bfbb-128">ダウンタイム ウィンドウの日時を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-128">You can then change the dates and times for the downtime window.</span></span>
    - <span data-ttu-id="3bfbb-129">要求を選択し、ツールバーの**キャンセル**を選択して、要求をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-129">Cancel the request by selecting the request and then selecting **Cancel** on the toolbar.</span></span>

## <a name="conditions-of-a-database-refresh"></a><span data-ttu-id="3bfbb-130">データベース更新の条件</span><span class="sxs-lookup"><span data-stu-id="3bfbb-130">Conditions of a database refresh</span></span>
<span data-ttu-id="3bfbb-131">データベース更新の操作の要件および条件の一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-131">Here is the list of requirements and conditions of operation for a database refresh:</span></span>

- <span data-ttu-id="3bfbb-132">要求は、要求を完了するためにリソースを確実に使用できるようにするため、目的のダウンタイム期間の 24 時間前までに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-132">Requests must be submitted 24 hours before the desired downtime window, to help guarantee that resources will be available to complete the request.</span></span>
- <span data-ttu-id="3bfbb-133">更新により、ターゲット環境の既存のデータベースが消去されます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-133">A refresh erases the existing database in the target environment.</span></span> <span data-ttu-id="3bfbb-134">更新が完了すると、既存のデータベースを復元することはできません。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-134">The existing database can't be recovered after the refresh is completed.</span></span>
- <span data-ttu-id="3bfbb-135">更新プロセスが完了するまで、ターゲット環境は使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-135">The target environment will be unavailable until the refresh process is completed.</span></span>
- <span data-ttu-id="3bfbb-136">リフレッシュは、Finance and Operations and Financial Reporting データベースにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-136">The refresh will affect only the Finance and Operations and Financial Reporting databases.</span></span>
- <span data-ttu-id="3bfbb-137">Azure blob storage のドキュメントは、ある環境から別の環境にコピーされません。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-137">Documents in Azure blob storage are not copied from one environment to another.</span></span> <span data-ttu-id="3bfbb-138">つまり、添付されたドキュメント処理ドキュメントとチームプレートは変更されず、現在の状態にとどまります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-138">This means that attached document handling documents and teamplates won't be changed and will remain in their current state.</span></span>
- <span data-ttu-id="3bfbb-139">管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーは無効になります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-139">All users except the Admin user and other internal service user accounts will be disabled.</span></span> <span data-ttu-id="3bfbb-140">このプロセスにより、他のユーザーをシステムに戻す前に、管理者ユーザーがデータを削除または難読化できます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-140">This process allows the Admin user to delete or obfuscate data before allowing others users back into the system.</span></span>
- <span data-ttu-id="3bfbb-141">管理者ユーザーは、特定のサービスまたは URL に統合エンドポイントを再接続するなど、必要な構成の変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-141">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>
- <span data-ttu-id="3bfbb-142">定期的にインポートおよびエクスポート ジョブされるすべてのデータ管理フレームワークは完全に処理され復元が開始される前にターゲット システムで停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-142">All data management framework recurring import and export jobs must be fully processed and stopped in the target system prior to initiating the restore.</span></span> <span data-ttu-id="3bfbb-143">さらに、すべての定期的なインポートおよびエクスポート ジョブが完全に処理された後に、データベースをソースから選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-143">In addition, we recommend that you select the database from the source after all recurring import and export jobs have been fully processed.</span></span> <span data-ttu-id="3bfbb-144">これにより、いずれかのシステムから Azure ストレージにオーファン ファイルが存在しないことが保証されます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-144">This will ensure there are no orphaned files in Azure storage from either system.</span></span> <span data-ttu-id="3bfbb-145">これは、データベースがターゲット環境にリストアされた後にオーファン ファイルを処理できないため重要です。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-145">This is important because orphaned files cannot be processed after the database is restored in the target environment.</span></span> <span data-ttu-id="3bfbb-146">復元後、統合ジョブを再開することができます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-146">After the restore, the integration jobs can be resumed.</span></span>
- <span data-ttu-id="3bfbb-147">実行するように設定されていたすべてのバッチは**源泉**状態として設定され、環境が再コンフィギュレーションされる前にバッチは実行を停止します。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-147">All batches that were set to run are set to **Withhold** status, to stop batches from running before the environment has been reconfigured.</span></span>
- <span data-ttu-id="3bfbb-148">SMTP サーバー構成、すべての電子メール アドレス、およびすべての **印刷管理**設定 (ネットワーク プリンターを含む) が削除されました。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-148">The SMTP server configuration, all email addresses, and all **Print management** settings, including network printers are removed.</span></span>
- <span data-ttu-id="3bfbb-149">LCS でプロジェクト所有者または環境マネージャーのロールを持つユーザーは、すべての非実稼働環境の SQL とマシンの資格情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3bfbb-149">Any user with a role of Project owner or Environment manager in LCS will have acccess to the SQL and machine credentials for all non-production environments.</span></span>

## <a name="steps-to-complete-after-a-database-refresh-for-environments-that-use-retail-functionality"></a><span data-ttu-id="3bfbb-150">Retail 機能を使用する環境のデータベース更新後に実行する手順</span><span class="sxs-lookup"><span data-stu-id="3bfbb-150">Steps to complete after a database refresh for environments that use Retail functionality</span></span>
[!include [environment-reprovision](../includes/environment-reprovision.md)]

