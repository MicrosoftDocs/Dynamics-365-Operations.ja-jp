---
title: データベース ポイントインタイム復元 (PITR)
description: このトピックでは、Finance and Operations のデータベースのポイントインタイム復元を実行する方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 016dc78f2d4b474551d3c797cd9ca4763e19f434
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183463"
---
# <a name="database-point-in-time-restore-pitr"></a><span data-ttu-id="87881-103">データベース ポイントインタイム復元 (PITR)</span><span class="sxs-lookup"><span data-stu-id="87881-103">Database point-in-time restore (PITR)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87881-104">Microsoft Dynamics Lifecycle Services (LCS) を使用し、サンドボックス ユーザー受け入れテスト (UAT) 環境のポイントインタイム復元 (PITR) を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="87881-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to perform the point-in-time restore (PITR) for a sandbox user acceptance testing (UAT) environment.</span></span> <span data-ttu-id="87881-105">Microsoft は、最大で30日間、 Microsoft Azure SQL の既定の設定にしたがって [自動化バックアップ](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) を維持します。</span><span class="sxs-lookup"><span data-stu-id="87881-105">Microsoft maintains [automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) according to Microsoft Azure SQL defaults, up to a maximum of 30 days.</span></span>  

## <a name="self-service-point-in-time-restore"></a><span data-ttu-id="87881-106">セルフサービスポイントインタイム復元</span><span class="sxs-lookup"><span data-stu-id="87881-106">Self-service point-in-time restore</span></span>
[!include [pitr](../includes/dbmovement-pitr.md)]

### <a name="restore-operation-failed"></a><span data-ttu-id="87881-107">失敗した操作の復元</span><span class="sxs-lookup"><span data-stu-id="87881-107">Restore operation failed</span></span>
<span data-ttu-id="87881-108">失敗した場合、**ロールバック**を実行するオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="87881-108">In case of failure, the option to perform a **Rollback** is available.</span></span>  <span data-ttu-id="87881-109">工程が最初に失敗した後にロールバック オプションをクリックすると、対象となるサンドボックス環境が復元の開始前の状態に戻されます。</span><span class="sxs-lookup"><span data-stu-id="87881-109">By clicking the rollback option after the operation has initially failed, your target sandbox environment will be restored to the state it was before the restore began.</span></span> <span data-ttu-id="87881-110">これにより、以前のデータベースが Azure SQL Server の削除されたデータベースの記憶域から復元されます。</span><span class="sxs-lookup"><span data-stu-id="87881-110">This will restore the previous database from the deleted databases storage on the Azure SQL Server.</span></span> <span data-ttu-id="87881-111">新しく復元されたデータでデータベースの同期を完了できないをターゲット サンドボックスにカスタマイズがある場合は、これがよく必要になります。</span><span class="sxs-lookup"><span data-stu-id="87881-111">This is often required if a customization is present in the target sandbox that cannot complete a database synchronization with the newly-restored data.</span></span>  

<span data-ttu-id="87881-112">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="87881-112">To determine the root cause of the failure, download the runbook logs using the available buttons before starting the rollback operation.</span></span>

### <a name="data-elements-that-need-attention-after-restore"></a><span data-ttu-id="87881-113">復元後に注意が必要なデータの要素</span><span class="sxs-lookup"><span data-stu-id="87881-113">Data elements that need attention after restore</span></span>
<span data-ttu-id="87881-114">前の時点からデータベースを復元する場合は、データベースがそのまま提供されることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="87881-114">When restoring a database from a previous point-in-time, keep in mind that the database is provided as-was.</span></span> <span data-ttu-id="87881-115">つまり、システム内のバッチ ジョブとその他のデータ要素は進行中の状態の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="87881-115">This means that batch jobs and other data elements in the system could be in an in-progress state.</span></span> <span data-ttu-id="87881-116">これらは、手動の確認が必要となります。</span><span class="sxs-lookup"><span data-stu-id="87881-116">These will require manual review.</span></span>

### <a name="environment-administrator"></a><span data-ttu-id="87881-117">環境管理者</span><span class="sxs-lookup"><span data-stu-id="87881-117">Environment administrator</span></span>
<span data-ttu-id="87881-118">対象となる環境のシステム管理者アカウント ('Admin' の UserId) は、ターゲットの web.config file ファイルにある値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="87881-118">The System Administrator account in the target environment (UserId of 'Admin') is reset to the value found in the web.config file on the target.</span></span>  <span data-ttu-id="87881-119">これは、Lifecycle Services の管理者と同じ値になります。</span><span class="sxs-lookup"><span data-stu-id="87881-119">This should be the same value as that of the Administrator from Lifecycle Services.</span></span> <span data-ttu-id="87881-120">これがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの **環境の詳細** ページにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="87881-120">To preview which account this will be, go to your target sandbox **Environment Details** page in LCS.</span></span>  <span data-ttu-id="87881-121">環境が最初に展開されたときに選択された **環境管理者** フィールドの値は、トランザクション データベース内のシステム管理者となるように更新されます。</span><span class="sxs-lookup"><span data-stu-id="87881-121">The value of the **Environment Administrator** field that was selected when the environment was first deployed is updated to be the System Administrator in the transactional database.</span></span> <span data-ttu-id="87881-122">これは、環境のテナントが環境管理者のテナントとなることも意味します。</span><span class="sxs-lookup"><span data-stu-id="87881-122">This also means that the tenant of the environment will be that of the Environment Administrator.</span></span>  

<span data-ttu-id="87881-123">web.config ファイルを別の値に変更するために環境で管理者ユーザー プロビジョニング ツールを使用した場合は、Lifecycle Services の内容と一致しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="87881-123">If you have used the Admin User Provisioning Tool on your environment to change the web.config file to a different value, it may not match what is in Lifecycle Services.</span></span>  <span data-ttu-id="87881-124">別のアカウントを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87881-124">If you require a different account, you will need to deallocate and delete the target sandbox, and redeploy by selecting another account.</span></span> <span data-ttu-id="87881-125">この後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。</span><span class="sxs-lookup"><span data-stu-id="87881-125">After this, you can perform another refresh database action to restore the data.</span></span>

## <a name="steps-to-complete-after-a-database-restore-for-environments-that-use-retail-functionality"></a><span data-ttu-id="87881-126">Retail 機能を使用する環境のデータベース復元後に実行する手順</span><span class="sxs-lookup"><span data-stu-id="87881-126">Steps to complete after a database restore for environments that use Retail functionality</span></span>
[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="known-issues"></a><span data-ttu-id="87881-127">既知の問題</span><span class="sxs-lookup"><span data-stu-id="87881-127">Known issues</span></span>

### <a name="point-in-time-restore-breaks-the-chain-of-available-restore-points"></a><span data-ttu-id="87881-128">ポイントインタイム復元により利用可能な復元ポイントのチェーンが壊れる</span><span class="sxs-lookup"><span data-stu-id="87881-128">Point-in-time restore breaks the chain of available restore points</span></span>
<span data-ttu-id="87881-129">復元データベース処理は、常に前の時点のスナップショットに基づいて新しいデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="87881-129">The restore database process always creates a new database based on a previous point-in-time snapshot.</span></span>  <span data-ttu-id="87881-130">このため、新しいデータベースには、復元の履歴はありませんが、今後使用される新しい復元ポイントを取得し始めます。</span><span class="sxs-lookup"><span data-stu-id="87881-130">Because of this, the new database does not have any restore history, but does begin to accrue new restore points going forward.</span></span> <span data-ttu-id="87881-131">つまり、ポイントインタイム復元を実行した後、同じ復元日時を使って復元することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="87881-131">This means that after performing point-in-time restore you will not be able to do so again using the same restore date and time.</span></span>  

<span data-ttu-id="87881-132">今後、Lifecycle Services チームは、削除されたデータベースの復元履歴を活用することで時点でポイントインタイム復元を向上させるよう努めます。</span><span class="sxs-lookup"><span data-stu-id="87881-132">Going forward, the Lifecycle Services team will work to improve point-in-time restore by leveraging the restore history of deleted databases.</span></span>  <span data-ttu-id="87881-133">これによって、破壊試験などのシナリオで同じ時点に継続的に復元できるようになります。</span><span class="sxs-lookup"><span data-stu-id="87881-133">This will allow continual restore back to the same point-in-time for scenarios such as destructive testing.</span></span>  <span data-ttu-id="87881-134">これは、LCS の今後のリリースで修正されます。</span><span class="sxs-lookup"><span data-stu-id="87881-134">This will be fixed in an upcoming release of LCS.</span></span>

### <a name="restore-is-denied-for-environments-running-platform-update-3-or-earlier"></a><span data-ttu-id="87881-135">プラットフォーム アップデート 3 以前を実行する環境で復元が拒否される</span><span class="sxs-lookup"><span data-stu-id="87881-135">Restore is denied for environments running Platform update 3 or earlier</span></span>
<span data-ttu-id="87881-136">環境でプラットフォーム更新 3 以前を実行している場合は、データベース復元の処理を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="87881-136">The restore database process cannot be completed if the environment is running Platform update 3 or earlier.</span></span> <span data-ttu-id="87881-137">詳細は、[現在サポートされているプラットフォーム更新の一覧](..//migration-upgrade/versions-update-policy.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87881-137">For more information, see the [list of currently supported Platform updates](..//migration-upgrade/versions-update-policy.md).</span></span>


