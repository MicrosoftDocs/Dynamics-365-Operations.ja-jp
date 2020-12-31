---
title: データベースのエクスポート
description: このトピックでは、Finance and Operations のデータベースをエクスポートする方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: aa3ddfdea3717bb5b7a34376ca9f4cbd1aca1db4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681082"
---
# <a name="export-a-database"></a>データベースのエクスポート

[!include [banner](../includes/banner.md)]

サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへのデータベースのエクスポートに Microsoft Dynamics Lifecycle Services (LCS) を使用できます。

## <a name="self-service-export-database"></a>セルフ サービスエクスポート データベース

[!include [dbmovement-export](../includes/dbmovement-export.md)]

### <a name="maximum-limit-50-gb-on-exported-bacapcs"></a>エクスポートされた bacapcs で最大 50 GB 
LCS からデータベースのエクスポートを実行するシステムを維持するために、最大 bacpac サイズの制限が設定されています。 この制限は、エクスポートする bacpac ごとに、50 GB に設定されます。 この制限の理由は次のとおりです。 

- 一元化されたシステムでは、同じ地域の複数の顧客に対してエクスポートを実行しています。このシステムは、ディスク領域に制限があります。  
- Azure SQL は、データを bacpac 形式で適切に圧縮します。多くの場合、顧客が 50 GB を超えると、カスタマイズ、またはバイナリ データがバックアップ ファイルのサイズは大幅に増加します。  

出力される bacpac のサイズが 50 GB を超えるためにエクスポートに失敗した場合、次の SQL スクリプトをサンドボックス データベースに対して実行して、上位 15 テーブルをメガバイト単位で特定してください。  データ エンティティのステージングに使用するすべてのテーブル (テーブル名の最後に「ステージング」が割り当てられます) は、切り捨てることができます。 バイナリまたは BLOB データを格納しているテーブル (JSON/XML/binary) はすべて切り捨てられるか、フィールドのコンテンツを削除して領域を解放する必要があります。 バイナリ データは圧縮できないので、データベース自体に大量のデータを格納すると、すぐに 50 GBの制限に達することになります。

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

### <a name="export-operation-failure"></a>エクスポート操作失敗

多くの場合、LCS のプロセスは、Microsoft Azure SQL データベースからの応答を待っている間にタイムアウトして、エクスポート処理を失敗してしまいます。 **経歴** ボタンを使用すると、LCS を進行中のエクスポート プロセスに再接続して、完了まで確認することができます。 エクスポートを開始してから 24 時間を超過した場合は、LCS プロジェクトの資産ライブラリの保留中の資産の期限が切れます。 この場合、エクスポート操作をロールバックして再起動する必要があります。

失敗したエクスポート操作をキャンセルするには、**ロールバック** ボタンを使用します。

### <a name="data-elements-that-arent-exported"></a>エクスポートされないデータ要素

環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。 次にいくつか例を挙げます。

* LogisticsElectronicAddress テーブル内の電子メール アドレス。
* BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。
* SysEmailParameters テーブルの SMTP 中継サーバー。
* PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。
* SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。
* DocuValue テーブル内のドキュメント添付ファイル。 これらの添付ファイルには、ソース環境で上書きされたすべての Microsoft Office テンプレートが含まれます。
* 管理者以外のすべてのユーザーは **無効** のステータスに設定されます。
* すべてのバッチ ジョブは、 **保留** 状態に設定されます。
* すべてのユーザーのパーティション値は "初期" パーティション レコード ID にリセットされます。
* 別のデータベースサーバーでは解読できないため、すべての Microsoft 暗号化フィールドはクリアされます。 次の例は、sysemailsmtppasswordテーブルの **パスワード** フィールドです。

### <a name="known-issues"></a>既知の問題

#### <a name="export-ran-for-some-time-and-then-reached-a-preparation-failed-state"></a>エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。

エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。 場合によっては、LCS から **再開** アクションを使用してエクスポート プロセスを復元することができます、 Lifecycle Services チームは既知のエラー コードを認識するよう努めており、データベースのエクスポート操作のログにこれらを追加することで、ユーザーが問題を解決できるようにします。 LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。 問題が発生した場合は、以下の「手動エクスポート」セクションに従って手動でのエクスポートを行うことができます。

#### <a name="export-doesnt-show-any-progress-in-lcs"></a>エクスポートで LCS に進捗状況が表示されない

エクスポートのプロセスは、他のデータベース移動の操作および、ランブックを使用しない一般的なパッケージ展開とは異なります。 したがって、LCS の進行状況インジケーターには、たとえ他のシナリオに通常は出力が表示されても、表示されません。 LCS チームは、ユーザーが解決策を見つけるため、データベースのエクスポート操作のログに追加されるように、既知のエラー コードを識別するよう努めています。 LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。
