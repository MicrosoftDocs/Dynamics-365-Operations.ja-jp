---
title: データベースのエクスポート
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースをエクスポートする方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 07/08/2019
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
ms.openlocfilehash: 19a5af0eb2720825865434c768a2fe042c881ce4
ms.sourcegitcommit: 3be8d2be6474264f0a530a052d19ea2635e269cf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/08/2019
ms.locfileid: "1729863"
---
# <a name="export-a-database"></a>データベースのエクスポート

[!include [banner](../includes/banner.md)]

サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへの Microsoft Dynamics 365 for Finance and Operations のデータベースのエクスポートの実行に Microsoft Dynamics Lifecycle Services (LCS) を使用できます。

## <a name="self-service-export-database"></a>セルフ サービスエクスポート データベース

[!include [dbmovement-export](../includes/dbmovement-export.md)]

### <a name="export-operation-failure"></a>エクスポート操作失敗

エクスポート操作が正常に行われない場合は、*ロールバック*できます。 操作が最初に失敗した後に**ロールバック** オプションをクリックすると、ソース サンドボックス環境がエクスポートの開始前の状態に戻されます。

失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。

### <a name="data-elements-that-arent-exported"></a>エクスポートされないデータ要素

環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。 次にいくつか例を挙げます。

* LogisticsElectronicAddress テーブル内の電子メール アドレス
* BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴
* SysEmailSMTPPassword テーブルの SMTP パスワード
* SysEmailParameters テーブルの SMTP 中継サーバー
* PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定
* SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード
* DocuValue テーブル内のドキュメント添付ファイル

さらに、管理者以外のすべてのユーザーが無効になり、すべてのバッチ ジョブのステータスが **保留** に設定されます。

## <a name="known-issues"></a>既知の問題

### <a name="export-ran-for-some-time-and-then-reached-a-preparation-failed-state"></a>エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。

エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。 場合によっては、LCS から **再開** アクションを使用してエクスポート プロセスを復元することができます、 Lifecycle Services チームは既知のエラー コードを認識するよう努めており、データベースのエクスポート操作のログにこれらを追加することで、ユーザーが問題を解決できるようにします。 LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。 問題が発生した場合は、 [レガシードキュメント](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/8bf1db9f2d994fc585caf380af85bb0a50eaf02b/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)をエクスポートすることによって手動でのエクスポートが可能となります。

### <a name="export-doesnt-show-any-progress-in-lcs"></a>エクスポートで LCS に進捗状況が表示されない

エクスポート プロセスは、ほかのデータベースの移動処理や一般的なパッケージの配備とは異なり、runbook を使用しません。 したがって、LCS の進行状況インジケーターには、それ以外のシナリオのような出力が表示されません。 Lifecycle Services チームは、LCS の将来のリリースではこの動作が改善されるよう努めています。 問題が発生した場合は、 [レガシードキュメント](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/8bf1db9f2d994fc585caf380af85bb0a50eaf02b/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)をエクスポートすることによって手動でのエクスポートが可能となります。
