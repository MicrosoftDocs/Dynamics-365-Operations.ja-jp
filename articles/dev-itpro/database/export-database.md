---
title: データベースのエクスポート
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースをエクスポートする方法について説明します。
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
ms.openlocfilehash: d604f485b3c5656cd3aee8a9a0ae70fa9993310f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550940"
---
# <a name="export-a-database"></a><span data-ttu-id="b7f10-103">データベースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="b7f10-103">Export a database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7f10-104">サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへの Microsoft Dynamics 365 for Finance and Operations のデータベースのエクスポートの実行に Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b7f10-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to export a database for Microsoft Dynamics 365 for Finance and Operations from a sandbox user acceptance testing (UAT) environment to the Asset library.</span></span>

## <a name="self-service-export-database"></a><span data-ttu-id="b7f10-105">セルフ サービスエクスポート データベース</span><span class="sxs-lookup"><span data-stu-id="b7f10-105">Self-service export database</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

### <a name="export-operation-failure"></a><span data-ttu-id="b7f10-106">エクスポート操作失敗</span><span class="sxs-lookup"><span data-stu-id="b7f10-106">Export operation failure</span></span>

<span data-ttu-id="b7f10-107">エクスポート操作が正常に行われない場合は、*ロールバック*できます。</span><span class="sxs-lookup"><span data-stu-id="b7f10-107">If the export operation isn't successful, you can do a *rollback*.</span></span> <span data-ttu-id="b7f10-108">操作が最初に失敗した後に**ロールバック** オプションをクリックすると、ソース サンドボックス環境がエクスポートの開始前の状態に戻されます。</span><span class="sxs-lookup"><span data-stu-id="b7f10-108">If you select the **Rollback** option after the initial failure of the operation, your source sandbox environment is restored to the state that it was in before the export began.</span></span>

<span data-ttu-id="b7f10-109">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b7f10-109">To determine the root cause of the failure, download the runbook logs by using the available buttons before you start the rollback operation.</span></span>

### <a name="data-elements-that-arent-exported"></a><span data-ttu-id="b7f10-110">エクスポートされないデータ要素</span><span class="sxs-lookup"><span data-stu-id="b7f10-110">Data elements that aren't exported</span></span>

<span data-ttu-id="b7f10-111">環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。</span><span class="sxs-lookup"><span data-stu-id="b7f10-111">When you export a database backup from an environment, some elements of the database aren't exported in the backup file.</span></span> <span data-ttu-id="b7f10-112">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="b7f10-112">Here are some examples:</span></span>

* <span data-ttu-id="b7f10-113">LogisticsElectronicAddress テーブル内の電子メール アドレス</span><span class="sxs-lookup"><span data-stu-id="b7f10-113">Email addresses in the LogisticsElectronicAddress table</span></span>
* <span data-ttu-id="b7f10-114">BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴</span><span class="sxs-lookup"><span data-stu-id="b7f10-114">Batch job history in the BatchJobHistory, BatchHistory, and BatchConstraintHistory tables</span></span>
* <span data-ttu-id="b7f10-115">SysEmailSMTPPassword テーブルの SMTP パスワード</span><span class="sxs-lookup"><span data-stu-id="b7f10-115">SMTP password in the SysEmailSMTPPassword table</span></span>
* <span data-ttu-id="b7f10-116">SysEmailParameters テーブルの SMTP 中継サーバー</span><span class="sxs-lookup"><span data-stu-id="b7f10-116">SMTP Relay server in the SysEmailParameters table</span></span>
* <span data-ttu-id="b7f10-117">PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定</span><span class="sxs-lookup"><span data-stu-id="b7f10-117">Print Management settings in the PrintMgmtSettings and PrintMgmtDocInstance tables</span></span>
* <span data-ttu-id="b7f10-118">SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード</span><span class="sxs-lookup"><span data-stu-id="b7f10-118">Environment-specific records in the SysServerConfig, SysServerSessions, SysCorpNetPrinters, SysClientSessions, BatchServerConfig, and BatchServerGroup tables</span></span>
* <span data-ttu-id="b7f10-119">DocuValue テーブル内のドキュメント添付ファイル</span><span class="sxs-lookup"><span data-stu-id="b7f10-119">Document attachments in the DocuValue table</span></span>

<span data-ttu-id="b7f10-120">さらに、管理者以外のすべてのユーザーが無効になり、すべてのバッチ ジョブのステータスが **保留** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b7f10-120">Additionally, all users except the admin are disabled, and all batch jobs are set to a status of **Withhold**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="b7f10-121">既知の問題</span><span class="sxs-lookup"><span data-stu-id="b7f10-121">Known issues</span></span>

### <a name="export-ran-for-some-time-and-then-reached-a-preparation-failed-state"></a><span data-ttu-id="b7f10-122">エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。</span><span class="sxs-lookup"><span data-stu-id="b7f10-122">Export ran for some time and then reached a "Preparation failed" state</span></span>

<span data-ttu-id="b7f10-123">エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。</span><span class="sxs-lookup"><span data-stu-id="b7f10-123">The export process can time out on Azure SQL Database when large databases are involved.</span></span> <span data-ttu-id="b7f10-124">場合によっては、LCS から **再開** アクションを使用してエクスポート プロセスを復元することができます、</span><span class="sxs-lookup"><span data-stu-id="b7f10-124">In some cases, the export process can be recovered by using the **Resume** action from LCS.</span></span> <span data-ttu-id="b7f10-125">Lifecycle Services チームは、ユーザーが解決策を見つけるため、データベースのエクスポート操作のログに追加できるように、既知のエラー コードを識別するよう努めています。</span><span class="sxs-lookup"><span data-stu-id="b7f10-125">The Lifecycle Services team is working to identify known error codes, so that it can add them to the logs for the export database operation to help guide users toward a resolution.</span></span> <span data-ttu-id="b7f10-126">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="b7f10-126">These known error codes will be added in a future release of LCS.</span></span>

### <a name="export-doesnt-show-any-progress-in-lcs"></a><span data-ttu-id="b7f10-127">エクスポートで LCS に進捗状況が表示されない</span><span class="sxs-lookup"><span data-stu-id="b7f10-127">Export doesn't show any progress in LCS</span></span>

<span data-ttu-id="b7f10-128">エクスポート プロセスは、runbook を使用しないという点で、他のデータベースの移動操作や一般的なパッケージ配置とも異なります。</span><span class="sxs-lookup"><span data-stu-id="b7f10-128">The export process differs from other database movement operations and also general package deployment in that it doesn't use a runbook.</span></span> <span data-ttu-id="b7f10-129">したがって、LCS の進行状況インジケーターには、それ以外のシナリオのような出力が表示されません。</span><span class="sxs-lookup"><span data-stu-id="b7f10-129">Therefore, the progress indicator in LCS doesn't show any output, as it would typically show in other scenarios.</span></span> <span data-ttu-id="b7f10-130">Lifecycle Services チームは、LCS の将来のリリースではこの動作が改善されるよう努めています。</span><span class="sxs-lookup"><span data-stu-id="b7f10-130">The Lifecycle Services team is working to improve this behavior in a future release of LCS.</span></span>
