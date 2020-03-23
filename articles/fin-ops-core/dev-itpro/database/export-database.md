---
title: データベースのエクスポート
description: このトピックでは、Finance and Operations のデータベースをエクスポートする方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 02/20/2020
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
ms.openlocfilehash: b790f96ce193e23c0044904d94aebb8968e24205
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113600"
---
# <a name="export-a-database"></a><span data-ttu-id="7bcc5-103">データベースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="7bcc5-103">Export a database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bcc5-104">サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへのデータベースのエクスポートに Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to export a database from a sandbox user acceptance testing (UAT) environment to the Asset library.</span></span>

## <a name="self-service-export-database"></a><span data-ttu-id="7bcc5-105">セルフ サービスエクスポート データベース</span><span class="sxs-lookup"><span data-stu-id="7bcc5-105">Self-service export database</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

### <a name="export-operation-failure"></a><span data-ttu-id="7bcc5-106">エクスポート操作失敗</span><span class="sxs-lookup"><span data-stu-id="7bcc5-106">Export operation failure</span></span>

<span data-ttu-id="7bcc5-107">多くの場合、LCS のプロセスは、Microsoft Azure SQL データベースからの応答を待っている間にタイムアウトして、エクスポート処理を失敗してしまいます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-107">Most often, export operations fail because the process in LCS times out while it's waiting for a response from Microsoft Azure SQL Database.</span></span> <span data-ttu-id="7bcc5-108">**経歴**ボタンを使用すると、LCS を進行中のエクスポート プロセスに再接続して、完了まで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-108">You can use the **Resume** button to reconnect LCS to the ongoing export process and see it through to completion.</span></span> <span data-ttu-id="7bcc5-109">エクスポートを開始してから 24 時間を超過した場合は、LCS プロジェクトの資産ライブラリの保留中の資産の期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-109">If more than 24 hours have passed since you began the export, the pending asset in the LCS Project asset library will be expired.</span></span> <span data-ttu-id="7bcc5-110">この場合、エクスポート操作をロールバックして再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-110">In this case, you must roll back the export operation and restart it.</span></span>

<span data-ttu-id="7bcc5-111">失敗したエクスポート操作をキャンセルするには、**ロールバック**ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-111">To cancel an export operation that has failed, you can use the **Rollback** button.</span></span>

### <a name="data-elements-that-arent-exported"></a><span data-ttu-id="7bcc5-112">エクスポートされないデータ要素</span><span class="sxs-lookup"><span data-stu-id="7bcc5-112">Data elements that aren't exported</span></span>

<span data-ttu-id="7bcc5-113">環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-113">When you export a database backup from an environment, some elements of the database aren't exported in the backup file.</span></span> <span data-ttu-id="7bcc5-114">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-114">Here are some examples:</span></span>

* <span data-ttu-id="7bcc5-115">LogisticsElectronicAddress テーブル内の電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-115">Email addresses in the LogisticsElectronicAddress table.</span></span>
* <span data-ttu-id="7bcc5-116">BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-116">Batch job history in the BatchJobHistory, BatchHistory, and BatchConstraintHistory tables.</span></span>
* <span data-ttu-id="7bcc5-117">SysEmailParameters テーブルの SMTP 中継サーバー。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-117">SMTP Relay server in the SysEmailParameters table.</span></span>
* <span data-ttu-id="7bcc5-118">PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-118">Print Management settings in the PrintMgmtSettings and PrintMgmtDocInstance tables.</span></span>
* <span data-ttu-id="7bcc5-119">SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-119">Environment-specific records in the SysServerConfig, SysServerSessions, SysCorpNetPrinters, SysClientSessions, BatchServerConfig, and BatchServerGroup tables.</span></span>
* <span data-ttu-id="7bcc5-120">DocuValue テーブル内のドキュメント添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-120">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="7bcc5-121">これらの添付ファイルには、ソース環境で上書きされたすべての Microsoft Office テンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-121">These attachments include any Microsoft Office templates that were overwritten in the source environment.</span></span>
* <span data-ttu-id="7bcc5-122">管理者以外のすべてのユーザーは **無効** のステータスに設定されます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-122">All users except the admin will be set to **Disabled** status.</span></span>
* <span data-ttu-id="7bcc5-123">すべてのバッチ ジョブは、 **保留** 状態に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-123">All batch jobs are set to **Withhold** status.</span></span>
* <span data-ttu-id="7bcc5-124">すべてのユーザーのパーティション値は "初期" パーティション レコード ID にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-124">All users will have their partition value reset to the "initial" partition record ID.</span></span>
* <span data-ttu-id="7bcc5-125">別のデータベースサーバーでは解読できないため、すべての Microsoft 暗号化フィールドはクリアされます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-125">All Microsoft-encrypted fields will be cleared, because they can't be decrypted on a different database server.</span></span> <span data-ttu-id="7bcc5-126">次の例は、sysemailsmtppasswordテーブルの **パスワード** フィールドです。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-126">An example is the **Password** field in the SysEmailSMTPPassword table.</span></span>

### <a name="known-issues"></a><span data-ttu-id="7bcc5-127">既知の問題</span><span class="sxs-lookup"><span data-stu-id="7bcc5-127">Known issues</span></span>

#### <a name="export-ran-for-some-time-and-then-reached-a-preparation-failed-state"></a><span data-ttu-id="7bcc5-128">エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-128">Export ran for some time and then reached a "Preparation failed" state</span></span>

<span data-ttu-id="7bcc5-129">エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-129">The export process can time out on Azure SQL Database when large databases are involved.</span></span> <span data-ttu-id="7bcc5-130">場合によっては、LCS から **再開** アクションを使用してエクスポート プロセスを復元することができます、</span><span class="sxs-lookup"><span data-stu-id="7bcc5-130">In some cases, the export process can be recovered by using the **Resume** action from LCS.</span></span> <span data-ttu-id="7bcc5-131">Lifecycle Services チームは既知のエラー コードを認識するよう努めており、データベースのエクスポート操作のログにこれらを追加することで、ユーザーが問題を解決できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-131">The Lifecycle Services team is working to identify known error codes, so these can be added to the logs for the export database operation to help guide users toward a resolution.</span></span> <span data-ttu-id="7bcc5-132">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-132">These known error codes will be added in a future release of LCS.</span></span> <span data-ttu-id="7bcc5-133">問題が発生した場合は、以下の「手動エクスポート」セクションに従って手動でのエクスポートを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-133">If you encounter an issue, you can manually export by following the “Manual export” section below.</span></span>

#### <a name="export-doesnt-show-any-progress-in-lcs"></a><span data-ttu-id="7bcc5-134">エクスポートで LCS に進捗状況が表示されない</span><span class="sxs-lookup"><span data-stu-id="7bcc5-134">Export doesn't show any progress in LCS</span></span>

<span data-ttu-id="7bcc5-135">エクスポートのプロセスは、他のデータベース移動の操作および、ランブックを使用しない一般的なパッケージ展開とは異なります。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-135">The export process differs from other database movement operations, and the general package deployment doesn't use a runbook.</span></span> <span data-ttu-id="7bcc5-136">したがって、LCS の進行状況インジケーターには、たとえ他のシナリオに通常は出力が表示されても、表示されません。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-136">Therefore, the progress indicator in LCS doesn't show any output, even though it typically shows output in other scenarios.</span></span> <span data-ttu-id="7bcc5-137">LCS チームは、ユーザーが解決策を見つけるため、データベースのエクスポート操作のログに追加されるように、既知のエラー コードを識別するよう努めています。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-137">The LCS team is working to identify known error codes so that they can be added to the logs for the export database operation to help guide users toward a resolution.</span></span> <span data-ttu-id="7bcc5-138">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="7bcc5-138">These known error codes will be added in a future release of LCS.</span></span>
