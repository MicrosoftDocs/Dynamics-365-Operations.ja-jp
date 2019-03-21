---
title: データベースのインポート
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースをインポートする方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/29/2019
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
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 77c20b406567fcd732281dcafedf4fbc896543a4
ms.sourcegitcommit: 0c1deb100d0bf6dacd14b328968bbc7a9d92583a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2019
ms.locfileid: "771214"
---
# <a name="import-a-database"></a><span data-ttu-id="543e4-103">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="543e4-103">Import a database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="543e4-104">サンドボックス ユーザー受け入れテスト (UAT) 環境への Microsoft Dynamics 365 for Finance and Operations のデータベースのインポートに Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="543e4-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to import a database for Microsoft Dynamics 365 for Finance and Operations into a sandbox user acceptance testing (UAT) environment.</span></span>

## <a name="self-service-import-database"></a><span data-ttu-id="543e4-105">セルフ サービス インポート データベース</span><span class="sxs-lookup"><span data-stu-id="543e4-105">Self-service import database</span></span>

[!include [dbmovement-import](../includes/dbmovement-import.md)]

### <a name="import-operation-failure"></a><span data-ttu-id="543e4-106">インポート操作失敗</span><span class="sxs-lookup"><span data-stu-id="543e4-106">Import operation failure</span></span>

<span data-ttu-id="543e4-107">インポート操作が正常に行われない場合は、*ロールバック*できます。</span><span class="sxs-lookup"><span data-stu-id="543e4-107">If the import operation isn't successful, you can do a *rollback*.</span></span> <span data-ttu-id="543e4-108">操作が最初に失敗した後に**ロールバック** オプションをクリックすると、対象となるサンドボックス環境がインポートの開始前の状態に戻されます。</span><span class="sxs-lookup"><span data-stu-id="543e4-108">If you select the **Rollback** option after the initial failure of the operation, your target sandbox environment is restored to the state that it was in before the import began.</span></span> <span data-ttu-id="543e4-109">ロールバック操作は、データベースを復元するための Microsoft Azure SQL データベース ポイントインタイム復元機能により使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="543e4-109">The rollback operation is made available by the Microsoft Azure SQL Database point-in-time restore capability for restoring the database.</span></span> <span data-ttu-id="543e4-110">ターゲット サンドボックスに存在するカスタマイズが、新しくインポートされたデータでデータベースの同期を完了できない場合、ロールバックがよく必要になります。</span><span class="sxs-lookup"><span data-stu-id="543e4-110">Rollback is often required if a customization that is present in the target sandbox can't complete a database synchronization with the newly imported data.</span></span>

<span data-ttu-id="543e4-111">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="543e4-111">To determine the root cause of the failure, download the runbook logs by using the available buttons before you start the rollback operation.</span></span>

### <a name="data-elements-that-require-attention-after-import"></a><span data-ttu-id="543e4-112">インポート後に注意が必要なデータの要素</span><span class="sxs-lookup"><span data-stu-id="543e4-112">Data elements that require attention after import</span></span>

<span data-ttu-id="543e4-113">データベースのバックアップをサンド ボックスUAT環境にインポートするときは、特定の活動を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="543e4-113">Specific activities must be completed when you import a database backup into a sandbox UAT environment.</span></span> <span data-ttu-id="543e4-114">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="543e4-114">Here are some examples:</span></span>

* <span data-ttu-id="543e4-115">お客様の要件に従って、電子メール機能が正しく再設定または無効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="543e4-115">Make sure that email capabilities are correctly reconfigured or turned off, according to your requirements.</span></span>
* <span data-ttu-id="543e4-116">お客様の要件に従って、統合設定がオンまたはオフになっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="543e4-116">Make sure that integration settings are turned on or off, according to your requirements.</span></span>
* <span data-ttu-id="543e4-117">Application Object Server (AOS) サーバーが必要なバッチ グループに追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="543e4-117">Make sure that Application Object Server (AOS) servers are added back to required batch groups.</span></span>
* <span data-ttu-id="543e4-118">システム ヘルプとタスク ガイドに再接続されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="543e4-118">Make sure that system Help and task guides are reconnected.</span></span>
* <span data-ttu-id="543e4-119">バッチ ジョブのステータスが**待機中**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="543e4-119">Make sure that batch jobs are set to a status of **Waiting**.</span></span>
* <span data-ttu-id="543e4-120">ユーザーが再度有効化されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="543e4-120">Make sure that users are re-enabled.</span></span>

### <a name="environment-admin"></a><span data-ttu-id="543e4-121">環境管理者</span><span class="sxs-lookup"><span data-stu-id="543e4-121">Environment admin</span></span>

<span data-ttu-id="543e4-122">対象となる環境のシステム管理者アカウント (**管理者**ユーザーID) が、その環境内の web.config ファイルに含まれる値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="543e4-122">The system admin account in the target environment (**Admin** user ID) is reset to the value that is found in the web.config file in that environment.</span></span> <span data-ttu-id="543e4-123">このアカウントは、LCS からの管理者アカウントと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="543e4-123">This account should be the same as the admin account from LCS.</span></span> <span data-ttu-id="543e4-124">このアカウントがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの **環境の詳細** ページにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="543e4-124">To preview which account this account will be, visit the **Environment details** page for your target sandbox in LCS.</span></span> <span data-ttu-id="543e4-125">環境が最初に展開されたときに **環境管理者** フィールドで選択された値は、トランザクション データベース内のシステム管理者となるように更新されます。</span><span class="sxs-lookup"><span data-stu-id="543e4-125">The value that was selected in the **Environment Administrator** field when the environment was first deployed is updated to the system admin in the transactional database.</span></span> <span data-ttu-id="543e4-126">これにより、環境のテナントが環境管理者のテナントになります。</span><span class="sxs-lookup"><span data-stu-id="543e4-126">Therefore, the tenant of the environment will be the tenant of the environment admin.</span></span>

<span data-ttu-id="543e4-127">web.config ファイルを変更するために環境に管理者ユーザー プロビジョニング ツールを使用した場合、値が LCS の値と一致しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="543e4-127">If you've used the Admin User Provisioning Tool on your environment to change the web.config file, the value might not match the value in LCS.</span></span> <span data-ttu-id="543e4-128">別のアカウントを使用することを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="543e4-128">If you require that a different account be used, you must deallocate and delete the target sandbox, redeploy, and select another account.</span></span> <span data-ttu-id="543e4-129">その後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。</span><span class="sxs-lookup"><span data-stu-id="543e4-129">You can then do another database refresh action to restore the data.</span></span>

## <a name="steps-to-complete-after-a-database-import-for-environments-that-use-retail-functionality"></a><span data-ttu-id="543e4-130">Retail 機能を使用する環境のデータベースインポート後に実行する手順</span><span class="sxs-lookup"><span data-stu-id="543e4-130">Steps to complete after a database import for environments that use Retail functionality</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="known-issues"></a><span data-ttu-id="543e4-131">既知の問題</span><span class="sxs-lookup"><span data-stu-id="543e4-131">Known issues</span></span>

### <a name="import-is-denied-for-environments-that-run-platform-update-3-or-earlier"></a><span data-ttu-id="543e4-132">プラットフォーム アップデート 3 以前を実行する環境でインポートが拒否される</span><span class="sxs-lookup"><span data-stu-id="543e4-132">Import is denied for environments that run Platform update 3 or earlier</span></span>

<span data-ttu-id="543e4-133">環境でプラットフォーム更新 3 以前を実行している場合は、データベース インポートの処理を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="543e4-133">The import database process can't be completed if the environment is running Platform update 3 or earlier.</span></span> <span data-ttu-id="543e4-134">現在サポートされているプラットフォーム更新の一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="543e4-134">See the list of currently supported platform updates.</span></span>
