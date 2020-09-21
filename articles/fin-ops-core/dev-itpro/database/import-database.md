---
title: データベースのインポート
description: このトピックでは、Finance and Operations アプリのデータベースをインポートする方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: fd9318418dee481153eb2fec9cac425e41ceedae
ms.sourcegitcommit: 0223e2d2276b9482f6ffdad643fc6a746f3b8469
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/21/2020
ms.locfileid: "3714647"
---
# <a name="import-a-database"></a><span data-ttu-id="99b26-103">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="99b26-103">Import a database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99b26-104">Microsoft Dynamics Lifecycle Services (LCS) は、ゴールデン コンフィギュレーション データベースをサンドボックス ユーザー受入テスト (UAT) の環境にインポートするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="99b26-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to import a golden configuration database into a sandbox user acceptance testing (UAT) environment.</span></span>

## <a name="self-service-import-database"></a><span data-ttu-id="99b26-105">セルフ サービス インポート データベース</span><span class="sxs-lookup"><span data-stu-id="99b26-105">Self-service import database</span></span>

[!include [dbmovement-import](../includes/dbmovement-import.md)]

### <a name="import-operation-failure"></a><span data-ttu-id="99b26-106">インポート操作失敗</span><span class="sxs-lookup"><span data-stu-id="99b26-106">Import operation failure</span></span>

<span data-ttu-id="99b26-107">インポート操作が正常に行われない場合は、*ロールバック*できます。</span><span class="sxs-lookup"><span data-stu-id="99b26-107">If the import operation isn't successful, you can do a *rollback*.</span></span> <span data-ttu-id="99b26-108">操作が最初に失敗した後に**ロールバック** オプションをクリックすると、対象となるサンドボックス環境がインポートの開始前の状態に戻されます。</span><span class="sxs-lookup"><span data-stu-id="99b26-108">If you select the **Rollback** option after the initial failure of the operation, your target sandbox environment is restored to the state that it was in before the import began.</span></span> <span data-ttu-id="99b26-109">ロールバック操作は、データベースを復元するための Microsoft Azure SQL データベース ポイントインタイム復元機能により使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="99b26-109">The rollback operation is made available by the Microsoft Azure SQL Database point-in-time restore capability for restoring the database.</span></span> <span data-ttu-id="99b26-110">ターゲット サンドボックスに存在するカスタマイズが、新しくインポートされたデータでデータベースの同期を完了できない場合、ロールバックがよく必要になります。</span><span class="sxs-lookup"><span data-stu-id="99b26-110">Rollback is often required if a customization that is present in the target sandbox can't complete a database synchronization with the newly imported data.</span></span>

### <a name="data-elements-that-require-attention-after-import"></a><span data-ttu-id="99b26-111">インポート後に注意が必要なデータの要素</span><span class="sxs-lookup"><span data-stu-id="99b26-111">Data elements that require attention after import</span></span>

<span data-ttu-id="99b26-112">データベースのバックアップをサンド ボックスUAT環境にインポートするときは、特定の活動を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99b26-112">Specific activities must be completed when you import a database backup into a sandbox UAT environment.</span></span> <span data-ttu-id="99b26-113">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="99b26-113">Here are some examples:</span></span>

* <span data-ttu-id="99b26-114">ソース データベースに、パーティション テーブルのレコードが 1 つしか含まれていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="99b26-114">Make sure that the source database contains only a single record in the Partitions table.</span></span>
* <span data-ttu-id="99b26-115">お客様の要件に従って、電子メール機能が正しく再設定または無効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="99b26-115">Make sure that email capabilities are correctly reconfigured or turned off, according to your requirements.</span></span>
* <span data-ttu-id="99b26-116">お客様の要件に従って、統合設定がオンまたはオフになっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="99b26-116">Make sure that integration settings are turned on or off, according to your requirements.</span></span>
* <span data-ttu-id="99b26-117">Application Object Server (AOS) サーバーが必要なバッチ グループに追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="99b26-117">Make sure that Application Object Server (AOS) servers are added back to required batch groups.</span></span>
* <span data-ttu-id="99b26-118">システム ヘルプとタスク ガイドに再接続されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99b26-118">Make sure that system Help and task guides are reconnected.</span></span>
* <span data-ttu-id="99b26-119">バッチ ジョブのステータスが**待機中**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99b26-119">Make sure that batch jobs are set to a status of **Waiting**.</span></span>
* <span data-ttu-id="99b26-120">ユーザーが再度有効化されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="99b26-120">Make sure that users are re-enabled.</span></span>

### <a name="environment-admin"></a><span data-ttu-id="99b26-121">環境管理者</span><span class="sxs-lookup"><span data-stu-id="99b26-121">Environment admin</span></span>

<span data-ttu-id="99b26-122">対象となる環境のシステム管理者アカウント (**管理者**ユーザーID) が、その環境内の web.config ファイルに含まれる値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="99b26-122">The system admin account in the target environment (**Admin** user ID) is reset to the value that is found in the web.config file in that environment.</span></span> <span data-ttu-id="99b26-123">このアカウントは、LCS からの管理者アカウントと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="99b26-123">This account should be the same as the admin account from LCS.</span></span> <span data-ttu-id="99b26-124">このアカウントがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの **環境の詳細** ページにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="99b26-124">To preview which account this account will be, visit the **Environment details** page for your target sandbox in LCS.</span></span> <span data-ttu-id="99b26-125">環境が最初に展開されたときに **環境管理者** フィールドで選択された値は、トランザクション データベース内のシステム管理者となるように更新されます。</span><span class="sxs-lookup"><span data-stu-id="99b26-125">The value that was selected in the **Environment Administrator** field when the environment was first deployed is updated to the system admin in the transactional database.</span></span> <span data-ttu-id="99b26-126">これにより、環境のテナントが環境管理者のテナントになります。</span><span class="sxs-lookup"><span data-stu-id="99b26-126">Therefore, the tenant of the environment will be the tenant of the environment admin.</span></span>

<span data-ttu-id="99b26-127">web.config ファイルを変更するために環境に管理者ユーザー プロビジョニング ツールを使用した場合、値が LCS の値と一致しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="99b26-127">If you've used the Admin User Provisioning Tool on your environment to change the web.config file, the value might not match the value in LCS.</span></span> <span data-ttu-id="99b26-128">別のアカウントを使用することを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99b26-128">If you require that a different account be used, you must deallocate and delete the target sandbox, redeploy, and select another account.</span></span> <span data-ttu-id="99b26-129">その後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。</span><span class="sxs-lookup"><span data-stu-id="99b26-129">You can then do another database refresh action to restore the data.</span></span>

## <a name="steps-to-complete-after-a-database-import-for-environments-that-use-commerce-functionality"></a><span data-ttu-id="99b26-130">コマース機能を使用する環境のデータベース インポート後に実行する手順</span><span class="sxs-lookup"><span data-stu-id="99b26-130">Steps to complete after a database import for environments that use Commerce functionality</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]
