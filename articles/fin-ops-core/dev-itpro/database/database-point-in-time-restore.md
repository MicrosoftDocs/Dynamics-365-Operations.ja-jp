---
title: データベース ポイントインタイム復元 (PITR)
description: このトピックでは、Finance and Operations のデータベースのポイントインタイム復元を実行する方法について説明します。
author: LaneSwenka
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f39905baad57a096f6b78aedc3c7ae3c2825056
ms.sourcegitcommit: 90a289962598394ad98209026013689322854b7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2021
ms.locfileid: "6092362"
---
# <a name="database-point-in-time-restore-pitr"></a><span data-ttu-id="60d0f-103">データベース ポイントインタイム復元 (PITR)</span><span class="sxs-lookup"><span data-stu-id="60d0f-103">Database point-in-time restore (PITR)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60d0f-104">Microsoft Dynamics Lifecycle Services (LCS) を使用し、サンドボックス ユーザー受け入れテスト (UAT) 環境のポイントインタイム復元 (PITR) を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to perform the point-in-time restore (PITR) for a sandbox user acceptance testing (UAT) environment.</span></span> <span data-ttu-id="60d0f-105">Microsoft は、業務および財務報告用のデータベースの[自動バックアップ](/azure/sql-database/sql-database-automated-backups)を、実稼働環境の場合は 28 日間、サンドボックス環境の場合は 14 日間維持します。</span><span class="sxs-lookup"><span data-stu-id="60d0f-105">Microsoft maintains [automated backups](/azure/sql-database/sql-database-automated-backups) of the business and financial reporting databases for 28 days for Production environments and 14 days for Sandbox environments.</span></span>

## <a name="self-service-point-in-time-restore"></a><span data-ttu-id="60d0f-106">セルフサービスポイントインタイム復元</span><span class="sxs-lookup"><span data-stu-id="60d0f-106">Self-service point-in-time restore</span></span>
[!include [pitr](../includes/dbmovement-pitr.md)]

### <a name="restore-operation-failed"></a><span data-ttu-id="60d0f-107">失敗した操作の復元</span><span class="sxs-lookup"><span data-stu-id="60d0f-107">Restore operation failed</span></span>
<span data-ttu-id="60d0f-108">失敗した場合、**ロールバック** を実行するオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-108">In the event of failure, the option to do a **rollback** is available.</span></span> <span data-ttu-id="60d0f-109">操作が最初に失敗をした後に ロールバック オプションを選択すると、ターゲット サンドボックス環境は、復元開始前の状態に復元されます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-109">If you select the rollback option after the operation originally fails, your target sandbox environment is restored to the state that it was in before the restore began.</span></span> <span data-ttu-id="60d0f-110">ターゲット サンドボックスに存在するカスタマイズが、新しく復元されたデータとのデータベースの同期を完了できない場合、ロールバックが必要になることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="60d0f-110">A rollback is often required if a customization that is present in the target sandbox environment can't complete a database synchronization with the newly restored data.</span></span>

<span data-ttu-id="60d0f-111">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="60d0f-111">To determine the root cause of the failure, download the runbook logs using the available buttons before starting the rollback operation.</span></span>

### <a name="data-elements-that-need-attention-after-restore"></a><span data-ttu-id="60d0f-112">復元後に注意が必要なデータの要素</span><span class="sxs-lookup"><span data-stu-id="60d0f-112">Data elements that need attention after restore</span></span>
<span data-ttu-id="60d0f-113">以前の時点からデータベースを復元する場合、データベースは "現状のまま" 提供されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="60d0f-113">When you restore a database from a previous point in time, keep in mind that the database is provided "as was."</span></span> <span data-ttu-id="60d0f-114">例えば、システム内のバッチ ジョブやその他のデータ要素が進行中の状態になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="60d0f-114">For example, batch jobs and other data elements in the system can be in an in-progress state.</span></span> <span data-ttu-id="60d0f-115">これらの要素は、手動で確認が必要となります。</span><span class="sxs-lookup"><span data-stu-id="60d0f-115">These elements will require manual review.</span></span>

> [!NOTE]
> <span data-ttu-id="60d0f-116">復元は、Azure Blob Storage に保存されているファイルへの参照を保存するテーブルに影響を与えます (ドキュメントの添付ファイルやカスタム Microsoft Office テンプレートなど)。</span><span class="sxs-lookup"><span data-stu-id="60d0f-116">Restore does affect the tables that store references to files stored in Azure blob storage (like document attachments and custom Microsoft Office templates).</span></span> <span data-ttu-id="60d0f-117">ただし、Azure Blob Storage 自体は、このプロセスの影響を受けません。復元時点の後に追加されたファイルは引き続き Azure Blob Storage に存在しますが、データベースには反映されません。</span><span class="sxs-lookup"><span data-stu-id="60d0f-117">However, as Azure blob storage itself is not affected by this process, any files added after the restore point will continue to exist in Azure blob storage but will not be reflected in the database.</span></span> 

### <a name="environment-administrator"></a><span data-ttu-id="60d0f-118">環境管理者</span><span class="sxs-lookup"><span data-stu-id="60d0f-118">Environment administrator</span></span>
<span data-ttu-id="60d0f-119">対象の環境のシステム管理者アカウント (**Admin** の **UserId** 値を持つアカウント) が、対象の環境に存在する web.config ファイルで検出された値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-119">The system administrator account in the target environment (that is, the account that has a **UserId** value of **Admin**) is reset to the value that is found in the web.config file in the target environment.</span></span> <span data-ttu-id="60d0f-120">この値は、LCS の管理者アカウントの値と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="60d0f-120">This value should match the value of the administrator account in LCS.</span></span> <span data-ttu-id="60d0f-121">使用するアカウントをプレビューするには、LCS でターゲット サンドボックス環境の **環境詳細** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="60d0f-121">To preview which account will be used, go to the **Environment Details** page for your target sandbox environment in LCS.</span></span> <span data-ttu-id="60d0f-122">環境が最初に展開されたときに **環境管理者** フィールドで選択された値は、トランザクション データベースのシステム管理者に更新されます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-122">The value that was selected in the **Environment Administrator** field when the environment was first deployed is updated to the system administrator in the transactional database.</span></span> <span data-ttu-id="60d0f-123">環境のテナントが環境管理者のテナントになります。</span><span class="sxs-lookup"><span data-stu-id="60d0f-123">The tenant of the environment will be the tenant of the environment administrator.</span></span>

<span data-ttu-id="60d0f-124">環境で管理者ユーザー プロビジョニング ツールを使用して、web.config ファイルの値を変更した場合、値は LCS の値と一致しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="60d0f-124">If you've used the Admin User Provisioning Tool in your environment to change the value in the web.config file, the value might not match the value in LCS.</span></span> <span data-ttu-id="60d0f-125">別のアカウントが必要な場合は、ターゲット サンドボックス環境の割り当てを解除して削除し、別のアカウントを選択して再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60d0f-125">If you require a different account, you must deallocate and delete the target sandbox environment, and then redeploy it by selecting another account.</span></span> <span data-ttu-id="60d0f-126">その後、データを復元するために別のデータベース更新アクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-126">You can then do another refresh database action to restore the data.</span></span>

## <a name="steps-to-complete-after-a-database-restore-for-environments-that-use-commerce-functionality"></a><span data-ttu-id="60d0f-127">コマース機能を使用する環境のデータベース復元後に実行する手順</span><span class="sxs-lookup"><span data-stu-id="60d0f-127">Steps to complete after a database restore for environments that use Commerce functionality</span></span>
[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="known-issues"></a><span data-ttu-id="60d0f-128">既知の問題</span><span class="sxs-lookup"><span data-stu-id="60d0f-128">Known issues</span></span>

### <a name="breaking-the-chain-of-available-restore-points"></a><span data-ttu-id="60d0f-129">使用可能な復元ポイントのチェーンの中断</span><span class="sxs-lookup"><span data-stu-id="60d0f-129">Breaking the chain of available restore points</span></span>
<span data-ttu-id="60d0f-130">頻繁に使用するいくつかのアクションは、以前に使用したデータベースと同じ復元ポイント履歴を持たない新しいデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="60d0f-130">Several frequently used actions create a new database that won't have the same restore point history as the previously used database.</span></span> <span data-ttu-id="60d0f-131">このアクションには、ポイント イン タイム復元、データベースの更新、データベースのインポート、実稼働環境からサンドボックス環境へのポイント イン タイム復元などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-131">These actions include point-in-time restores, database refreshes, database imports, and point-in-time restores from the production environment to the sandbox environment.</span></span> <span data-ttu-id="60d0f-132">さらに、データベースの更新時に環境に適用するソフトウェア展開可能なパッケージが失敗し、LCS のロールバック機能を使用する場合、ロールバック機能はデータベースのポイント イン タイム復元を実行し、その復元は新しいデータベースも作成します。</span><span class="sxs-lookup"><span data-stu-id="60d0f-132">In addition, if a software deployable package that you apply to your environment fails during update of the database, and you use the rollback functionality in LCS, the rollback functionality does a point-in-time restore of the database, and that restore also creates a new database.</span></span> 

<span data-ttu-id="60d0f-133">新しいデータベースには、復元ポイント履歴はありませんが、その時点から新しい復元ポイントを取得し始めます。</span><span class="sxs-lookup"><span data-stu-id="60d0f-133">Although the new database doesn't have any restore point history, it does begin to accrue new restore points from that time onward.</span></span> <span data-ttu-id="60d0f-134">前述のアクションのいずれかを実行した後、同じ復元日時を使用して再度実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="60d0f-134">After you perform any of the previously mentioned actions, you can't perform it again by using the same restore date and time.</span></span>

### <a name="restore-is-denied-for-environments-that-run-platform-update-20-or-earlier"></a><span data-ttu-id="60d0f-135">プラットフォーム 更新プログラム 20 以前が稼働している環境では、復元は拒否されます</span><span class="sxs-lookup"><span data-stu-id="60d0f-135">Restore is denied for environments that run Platform update 20 or earlier</span></span>
<span data-ttu-id="60d0f-136">環境でプラットフォーム更新 20 以前を実行している場合は、データベース復元の処理を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="60d0f-136">The restore database process cannot be completed if the environment is running Platform update 20 or earlier.</span></span> <span data-ttu-id="60d0f-137">詳細については、[ソフトウェアのライフサイクル ポリシーとクラウド リリース](..//migration-upgrade/versions-update-policy.md)で現在サポートされているプラットフォーム更新の一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60d0f-137">For more information, see the list of currently supported Platform updates in the [Software lifecycle policy and cloud releases](..//migration-upgrade/versions-update-policy.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
