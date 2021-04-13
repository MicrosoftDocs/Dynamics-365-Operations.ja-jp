---
title: データベースのエクスポート
description: このトピックでは、Finance and Operations のデータベースをエクスポートする方法について説明します。
author: LaneSwenka
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: b54a68feb3b726fb7238b910770b253cc573ee5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753044"
---
# <a name="export-a-database"></a><span data-ttu-id="50777-103">データベースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="50777-103">Export a database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50777-104">サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへのデータベースのエクスポートに Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="50777-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to export a database from a sandbox user acceptance testing (UAT) environment to the Asset library.</span></span>

## <a name="self-service-export-database"></a><span data-ttu-id="50777-105">セルフ サービスエクスポート データベース</span><span class="sxs-lookup"><span data-stu-id="50777-105">Self-service export database</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

### <a name="maximum-limit-50-gb-on-exported-bacpacs"></a><span data-ttu-id="50777-106">エクスポートされた bacpacs で最大 50 GB</span><span class="sxs-lookup"><span data-stu-id="50777-106">Maximum limit 50 GB on exported bacpacs</span></span> 
<span data-ttu-id="50777-107">LCS からデータベースのエクスポートを実行するシステムを維持するために、最大 bacpac サイズの制限が設定されています。</span><span class="sxs-lookup"><span data-stu-id="50777-107">To maintain the system that performs database export from LCS, a limit on the maximum bacpac size is being imposed.</span></span> <span data-ttu-id="50777-108">この制限は、エクスポートする bacpac ごとに、50 GB に設定されます。</span><span class="sxs-lookup"><span data-stu-id="50777-108">This limit is set at 50 GB for each bacpac exported.</span></span> <span data-ttu-id="50777-109">この制限の理由は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="50777-109">The reasons for this limit include:</span></span> 

- <span data-ttu-id="50777-110">一元化されたシステムでは、同じ地域の複数の顧客に対してエクスポートを実行しています。このシステムは、ディスク領域に制限があります。</span><span class="sxs-lookup"><span data-stu-id="50777-110">A centralized system is performing the exports for multiple customers in the same geographic region, and this system has constraints on disk space.</span></span>  
- <span data-ttu-id="50777-111">Azure SQL は、データを bacpac 形式で適切に圧縮します。多くの場合、顧客が 50 GB を超えると、カスタマイズ、またはバイナリ データがバックアップ ファイルのサイズは大幅に増加します。</span><span class="sxs-lookup"><span data-stu-id="50777-111">Azure SQL neatly compresses the data in the bacpac format and in many cases, where customers exceed 50 GB, customizations or binary data drastically oversize the backup file.</span></span>  

<span data-ttu-id="50777-112">出力される bacpac のサイズが 50 GB を超えるためにエクスポートに失敗した場合、次の SQL スクリプトをサンドボックス データベースに対して実行して、上位 15 テーブルをメガバイト単位で特定してください。</span><span class="sxs-lookup"><span data-stu-id="50777-112">If you experience an export failure because the resulting bacpac is over 50 GB in size, try running the following SQL script against your sandbox database to identify the top 15 tables by size in megabytes.</span></span>  <span data-ttu-id="50777-113">データ エンティティのステージングに使用するすべてのテーブル (テーブル名の最後に「ステージング」が割り当てられます) は、切り捨てることができます。</span><span class="sxs-lookup"><span data-stu-id="50777-113">Any tables that are for data entity staging (they will have "staging" at the end of the table name) can be truncated.</span></span> <span data-ttu-id="50777-114">バイナリまたは BLOB データを格納しているテーブル (JSON/XML/binary) はすべて切り捨てられるか、フィールドのコンテンツを削除して領域を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50777-114">Any tables that are storing binary or blob data (JSON/XML/binary) should either be truncated or the contents of that field should be deleted to free up space.</span></span> <span data-ttu-id="50777-115">バイナリ データは圧縮できないので、データベース自体に大量のデータを格納すると、すぐに 50 GBの制限に達することになります。</span><span class="sxs-lookup"><span data-stu-id="50777-115">Binary data cannot be compressed, so storing large volumes of data in the database itself will cause you to quickly reach the 50 GB limit.</span></span>

```sql
USE [YourDBName] -- replace your dbname
GO
SELECT top 15
s.Name AS SchemaName,
t.Name AS TableName,
p.rows AS RowCounts,
CAST(ROUND((SUM(a.used_pages) / 128.00), 2) AS NUMERIC(36, 2)) AS Used_MB,
CAST(ROUND((SUM(a.total_pages) - SUM(a.used_pages)) / 128.00, 2) AS NUMERIC(36, 2)) AS Unused_MB,
CAST(ROUND((SUM(a.total_pages) / 128.00), 2) AS NUMERIC(36, 2)) AS Total_MB
FROM sys.tables t
INNER JOIN sys.indexes i ON t.OBJECT_ID = i.object_id
INNER JOIN sys.partitions p ON i.object_id = p.OBJECT_ID AND i.index_id = p.index_id
INNER JOIN sys.allocation_units a ON p.partition_id = a.container_id
INNER JOIN sys.schemas s ON t.schema_id = s.schema_id
GROUP BY t.Name, s.Name, p.Rows
ORDER BY Total_MB DESC
GO
```

### <a name="export-operation-failure"></a><span data-ttu-id="50777-116">エクスポート操作失敗</span><span class="sxs-lookup"><span data-stu-id="50777-116">Export operation failure</span></span>

<span data-ttu-id="50777-117">多くの場合、LCS のプロセスは、Microsoft Azure SQL データベースからの応答を待っている間にタイムアウトして、エクスポート処理を失敗してしまいます。</span><span class="sxs-lookup"><span data-stu-id="50777-117">Most often, export operations fail because the process in LCS times out while it's waiting for a response from Microsoft Azure SQL Database.</span></span> <span data-ttu-id="50777-118">**経歴** ボタンを使用すると、LCS を進行中のエクスポート プロセスに再接続して、完了まで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="50777-118">You can use the **Resume** button to reconnect LCS to the ongoing export process and see it through to completion.</span></span> <span data-ttu-id="50777-119">エクスポートを開始してから 24 時間を超過した場合は、LCS プロジェクトの資産ライブラリの保留中の資産の期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="50777-119">If more than 24 hours have passed since you began the export, the pending asset in the LCS Project asset library will be expired.</span></span> <span data-ttu-id="50777-120">この場合、エクスポート操作をロールバックして再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50777-120">In this case, you must roll back the export operation and restart it.</span></span>

<span data-ttu-id="50777-121">失敗したエクスポート操作をキャンセルするには、**ロールバック** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="50777-121">To cancel an export operation that has failed, you can use the **Rollback** button.</span></span>

### <a name="data-elements-that-arent-exported"></a><span data-ttu-id="50777-122">エクスポートされないデータ要素</span><span class="sxs-lookup"><span data-stu-id="50777-122">Data elements that aren't exported</span></span>

<span data-ttu-id="50777-123">環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。</span><span class="sxs-lookup"><span data-stu-id="50777-123">When you export a database backup from an environment, some elements of the database aren't exported in the backup file.</span></span> <span data-ttu-id="50777-124">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="50777-124">Here are some examples:</span></span>

* <span data-ttu-id="50777-125">**LogisticsElectronicAddress** テーブル内の電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="50777-125">Email addresses in the **LogisticsElectronicAddress** table.</span></span>
* <span data-ttu-id="50777-126">**BatchJobHistory**、**BatchHistory**、および **BatchConstraintsHistory** テーブルのバッチ ジョブ履歴。</span><span class="sxs-lookup"><span data-stu-id="50777-126">Batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintsHistory** tables.</span></span>
* <span data-ttu-id="50777-127">**SysEmailParameters** テーブルの SMTP 中継サーバー。</span><span class="sxs-lookup"><span data-stu-id="50777-127">SMTP Relay server in the **SysEmailParameters** table.</span></span>
* <span data-ttu-id="50777-128">**PrintMgmtSettings** と **PrintMgmtDocInstance** テーブルの印刷管理設定。</span><span class="sxs-lookup"><span data-stu-id="50777-128">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables.</span></span>
* <span data-ttu-id="50777-129">**SysServerConfig**、**SysServerSessions**、**SysCorpNetPrinters**、**SysClientSessions**、 **BatchServerConfig**、および **BatchServerGroup** テーブル内の環境固有のレコード。</span><span class="sxs-lookup"><span data-stu-id="50777-129">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables.</span></span>
* <span data-ttu-id="50777-130">**DocuValue** テーブル内のドキュメント添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="50777-130">Document attachments in the **DocuValue** table.</span></span> <span data-ttu-id="50777-131">これらの添付ファイルには、ソース環境で上書きされたすべての Microsoft Office テンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="50777-131">These attachments include any Microsoft Office templates that were overwritten in the source environment.</span></span>
* <span data-ttu-id="50777-132">管理者以外のすべてのユーザーは **無効** のステータスに設定されます。</span><span class="sxs-lookup"><span data-stu-id="50777-132">All users except the admin will be set to **Disabled** status.</span></span>
* <span data-ttu-id="50777-133">すべてのバッチ ジョブは、 **保留** 状態に設定されます。</span><span class="sxs-lookup"><span data-stu-id="50777-133">All batch jobs are set to **Withhold** status.</span></span>
* <span data-ttu-id="50777-134">すべてのユーザーのパーティション値は "初期" パーティション レコード ID にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="50777-134">All users will have their partition value reset to the "initial" partition record ID.</span></span>
* <span data-ttu-id="50777-135">別のデータベースサーバーでは解読できないため、すべての Microsoft 暗号化フィールドはクリアされます。</span><span class="sxs-lookup"><span data-stu-id="50777-135">All Microsoft-encrypted fields will be cleared, because they can't be decrypted on a different database server.</span></span> <span data-ttu-id="50777-136">次の例は、**SysEmailSMTPPassword** テーブルの **パスワード** フィールドです。</span><span class="sxs-lookup"><span data-stu-id="50777-136">An example is the **Password** field in the **SysEmailSMTPPassword** table.</span></span>


### <a name="known-issues"></a><span data-ttu-id="50777-137">既知の問題</span><span class="sxs-lookup"><span data-stu-id="50777-137">Known issues</span></span>

#### <a name="export-ran-for-some-time-and-then-reached-a-preparation-failed-state"></a><span data-ttu-id="50777-138">エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。</span><span class="sxs-lookup"><span data-stu-id="50777-138">Export ran for some time and then reached a "Preparation failed" state</span></span>

<span data-ttu-id="50777-139">エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。</span><span class="sxs-lookup"><span data-stu-id="50777-139">The export process can time out on Azure SQL Database when large databases are involved.</span></span> <span data-ttu-id="50777-140">場合によっては、LCS から **再開** アクションを使用してエクスポート プロセスを復元することができます、</span><span class="sxs-lookup"><span data-stu-id="50777-140">In some cases, the export process can be recovered by using the **Resume** action from LCS.</span></span> <span data-ttu-id="50777-141">Lifecycle Services チームは既知のエラー コードを認識するよう努めており、データベースのエクスポート操作のログにこれらを追加することで、ユーザーが問題を解決できるようにします。</span><span class="sxs-lookup"><span data-stu-id="50777-141">The Lifecycle Services team is working to identify known error codes, so these can be added to the logs for the export database operation to help guide users toward a resolution.</span></span> <span data-ttu-id="50777-142">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="50777-142">These known error codes will be added in a future release of LCS.</span></span> 

#### <a name="export-doesnt-show-any-progress-in-lcs"></a><span data-ttu-id="50777-143">エクスポートで LCS に進捗状況が表示されない</span><span class="sxs-lookup"><span data-stu-id="50777-143">Export doesn't show any progress in LCS</span></span>

<span data-ttu-id="50777-144">エクスポートのプロセスは、他のデータベース移動の操作および、ランブックを使用しない一般的なパッケージ展開とは異なります。</span><span class="sxs-lookup"><span data-stu-id="50777-144">The export process differs from other database movement operations, and the general package deployment doesn't use a runbook.</span></span> <span data-ttu-id="50777-145">したがって、LCS の進行状況インジケーターには、たとえ他のシナリオに通常は出力が表示されても、表示されません。</span><span class="sxs-lookup"><span data-stu-id="50777-145">Therefore, the progress indicator in LCS doesn't show any output, even though it typically shows output in other scenarios.</span></span> <span data-ttu-id="50777-146">LCS チームは、ユーザーが解決策を見つけるため、データベースのエクスポート操作のログに追加されるように、既知のエラー コードを識別するよう努めています。</span><span class="sxs-lookup"><span data-stu-id="50777-146">The LCS team is working to identify known error codes so that they can be added to the logs for the export database operation to help guide users toward a resolution.</span></span> <span data-ttu-id="50777-147">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="50777-147">These known error codes will be added in a future release of LCS.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]