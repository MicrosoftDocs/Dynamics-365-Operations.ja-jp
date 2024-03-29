---
title: データベースの更新
description: この記事では、Microsoft Dynamics 365 Finance のデータベースの更新を実行する方法について説明します。
author: LaneSwenka
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.custom: 257614
ms.assetid: 558598db-937e-4bfe-80c7-a861be021db1
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-09-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45e59d15a0aa17940825569fb5ab22cad88a8ab0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867554"
---
# <a name="refresh-database"></a>データベースの更新

[!include [banner](../includes/banner.md)]

サンドボックス ユーザー受け入れテスト (UAT) 環境に対するデータベースの更新の実行に、Microsoft Dynamics Lifecycle Services (LCS) を使用することができます。 データベースの更新対象となるサンド ボックス UAT 環境に、運用環境のトランザクションおよび財務報告データベースをコピーできます。 別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス UAT 環境にデータベースをコピーすることもできます。

> [!IMPORTANT]
> 営業時間中またはピーク時に運用データをコピーすると、生産システムに影響を与える可能性があります。 データベースの更新は、オフピーク時に行い、一度に 1 つの更新操作のみを制限することを強くお勧めします。
>
> 運用レポートを目的としてサンドボックス環境に運用データをコピーすることはできません。

## <a name="self-service-database-refresh"></a>データベースのセルフ サービスエ更新
人手または手動のプロセスに依存しないでお客様にデータ アプリケーション ライフサイクル管理 (*DataALM* とも呼ばれます) 機能を提供することを目標として、Lifecycle Services チームは自動化された **データベースの更新** アクションを導入しました。 このプロセスの概要を以下に示します。

1. **環境の詳細** ページで 対象のサンドボックスを確認し 、メニューオプションの **メンテナンス** \> **データベースの移動** をクリックします。
2. **データベースの選択** オプションを選択し、ソース環境を選択します。
3. 警告に注意し、ソース環境からコピーされていないデータの要素の一覧を確認します。
4. 更新操作がすぐに開始されます。

### <a name="refresh-operation-failed"></a>更新操作が失敗しました
失敗した場合、ロールバックを実行するオプションを使用できます。  工程が最初に失敗した後に **ロールバック** オプションをクリックすると、対象となるサンドボックス環境が更新の開始前の状態に戻されます。 Azure SQL ポイントインタイム復元機能により、データベースを復元できるようになります。 新しく更新されたデータでデータベースの同期を完了できないをターゲット サンドボックスにカスタマイズがある場合は、これがよく必要になります。

失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。  

### <a name="data-elements-that-arent-copied-during-refresh"></a>更新中にはコピーされないデータ要素
このセクションの情報は、データベースの更新操作中にターゲット環境にコピーされないデータベースの特定の要素を一覧表示します。

#### <a name="when-refreshing-a-production-environment-to-a-sandbox-environment-or-a-sandbox-to-another-sandbox-environment"></a>サンドボックス環境またはサンドボックスから別のサンドボックス環境に運用環境を更新する場合

* LogisticsElectronicAddress テーブル内の電子メール アドレス。
* SysEmailParameters テーブルの SMTP 中継サーバー。
* PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。
* 管理者以外のすべてのユーザーは **無効** のステータスに設定されます。

#### <a name="when-refreshing-from-sandbox-environment-to-production-environment"></a>サンドボックス環境から運用環境に更新する場合
これは、[ゴールデン構成プロモーション](dbmovement-scenario-goldenconfig.md) とも呼ばれます。
* バッチ ジョブ履歴は、BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルに格納されています。

#### <a name="these-elements-are-removed-for-all-database-refresh-operations"></a>これらの要素は、すべてのデータベースの更新操作で削除されます

* SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。
* Azure Blob Storage に保存されているすべてのファイル。 これには、ドキュメントの添付ファイル (DocuValue テーブルおよび DocuDeletedValue テーブルから)、およびカスタム Microsoft Office テンプレート (DocuTemplate テーブルから) が含まれます。
* すべてのバッチ ジョブは、 **保留** 状態に設定されます。
* すべてのユーザーのパーティション値は "初期" パーティション レコード ID にリセットされます。
* 別のデータベースサーバーでは解読できないため、すべての Microsoft 暗号化フィールドはクリアされます。 次の例は、sysemailsmtppasswordテーブルの **パスワード** フィールドです。
* [メンテナンス モード](../sysadmin/maintenance-mode.md) 設定は、ソースで有効になっていた場合でも無効になります。
* 二重書き込みの構成。  この操作に成功した後にターゲット環境に新しいリンクを設定するには、[二重書き込み環境リンク](../data-entities/dual-write/link-your-environment.md)を参照してください。
* いくつかの[エンティティの変更追跡](../data-entities/entity-change-track.md) は無効になります。

これらの要素は、環境固有のものであるためコピーされません。 この例には、BatchServerConfigおよびSysCorpNetPrintersの各レコードが含まれます。 その他の要素は、サポート チケットのデータ量が多くなる懸念があるためコピーされません。 たとえば、簡易メール転送プロトコル (SMTP) はUAT環境でも有効になっているため、重複する電子メールが送信されてしまう可能性があります。また、バッチジョブも有効になっているため、無効な統合メッセージが送信されてしまう可能性もあるため、管理者がポストリフレッシュクリーンアップを行う前にユーザーが有効化されてしまう可能性があります。

### <a name="environment-administrator"></a>環境管理者
対象となる環境のシステム管理者アカウント ('Admin' の UserId) は、ターゲットの web.config file ファイルにある値にリセットされます。  これは、Lifecycle Services の管理者と同じ値になります。  これがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの **環境の詳細** ページにアクセスします。  環境が最初に展開されたときに選択された **環境管理者** フィールドの値は、トランザクション データベース内のシステム管理者となるように更新されます。 これは、環境のテナントが環境管理者のテナントとなることも意味します。

web.config ファイルを別の値に変更するために環境で管理者ユーザー プロビジョニング ツールを使用した場合は、Lifecycle Services の内容と一致しない可能性があります。  別のアカウントを使用することを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。 この後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。

あるテナントから別のテナントに環境を更新することはできません。 この制限は、onmicrosoft.com テナントにも適用されます。 ソース環境とターゲット環境の管理者アカウントが、同じテナント ドメインからのものであることを確認する必要があります。

### <a name="conditions-of-a-database-refresh"></a>データベース更新の条件
データベース更新の操作の要件および条件の一覧を次に示します。

- 更新処理では、実行対象のデータベースで削除が実行されます。
- ターゲット環境は、データベースのコピーがターゲット サーバーに達するまで使用可能です。 その時点以降は、更新プロセスが完了するまで、ターゲット環境はオフラインになります。
- リフレッシュは、アプリケーションおよび Financial Reporting データベースにのみ影響します。
-  ある環境から別の環境に、**Azure Blob Storage に保管してあるファイルはコピー** されません。 これには、**ドキュメントの添付ファイルやカスタム Microsoft Office テンプレート** が含まれます。 これらのドキュメントは変更されず、現在の状態のままになります。 
- 管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーは使用できなくなります。 このプロセスにより、ほかのユーザーがシステムに復帰する前に管理者ユーザーがデータを削除または難読化できます。
- 管理者ユーザーは、特定のサービスまたは URL に統合エンドポイントを再接続するなど、必要な構成の変更を加える必要があります。
- 定期的なインポートおよびエクスポート ジョブを持つすべてのデータ管理フレームワークは完全に処理され復元が開始される前にターゲット システムで停止する必要があります。 さらに、すべての定期的なインポートおよびエクスポート ジョブが完全に処理された後に、データベースをソースから選択することをお勧めします。 これにより、いずれかのシステムから Azure ストレージにオーファン ファイルが存在しないことが保証されます。 これは、データベースがターゲット環境にリストアされた後にオーファン ファイルを処理できないため重要です。 復元後、統合ジョブを再開することができます。
- LCS でプロジェクト所有者または環境マネージャーのロールを持つユーザーは、すべての非運用環境の SQL とマシンの資格情報にアクセスできます。
- データベースが Spartan で管理されていない場合は、データベースを同じ地理上の Azure リージョンでホストする必要があります。  SQL server の完全修飾アドレスの一部に ' spartan ' が含まれていれば、データベースは Spartan に管理されています。
- 実行元の環境で割り当てられたデータベースの容量は、実行対象の環境のデータベースの最大容量よりも小さくする必要があります。

## <a name="steps-to-complete-after-a-database-refresh-for-environments-that-use-commerce-functionality"></a>コマース機能を使用する環境のデータベース更新後に実行する手順
[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="known-issues"></a>既知の問題

### <a name="the-restore-operation-fails-if-the-sandbox-customizations-are-incompatible-with-production-data"></a>サンドボックスのカスタマイズが運用データと互換性がない場合、復元操作は失敗します

カスタマイズがサンドボックス環境に正常に追加された場合 (つまり、顧客の AOT 配置可能パッケージが LCS 経由で正常にインストールされた場合)、運用データに対して成功しない可能性があります。 たとえば、顧客が **仕入先名** の一意のインデックスを VendTable テーブルに追加します。 このカスタマイズは、サンドボックス環境に重複した仕入先名がない場合、正常にインストールされます。 ただし、運用データベースを復元操作の一環として使用した場合、サンドボックス環境にインバウンドするデータセットに重複があると、インストールが失敗することがあります。 このデータセットの重複はサポートされていません。 したがって、復元操作を成功させる前に、カスタマイズを削除する必要があります。

### <a name="refresh-is-denied-for-environments-that-run-platform-update-20-or-earlier"></a>プラットフォーム 更新プログラム 20 以前が稼働している環境では、更新処理は拒否されます
現在、環境がプラットフォーム更新プログラム 20 またはそれ以前を実行している場合は、データベースの更新プロセスを完了することはできません。 詳細については、[現在サポートされているプラットフォーム更新の一覧](../migration-upgrade/versions-update-policy.md) を参照してください。

### <a name="incompatible-version-of-financial-reporting-between-source-and-target-environments"></a>ソース環境とターゲット環境間での財務報告の互換性のないバージョン
実行対象とする環境の財務報告のバージョンが実行元の環境よりも古い場合は、データベースの更新プロセス (セルフサービスまたはサービス要求経由) を正常に完了できません。 この問題を解決するには、両方の環境で財務報告が最新バージョンとなるように更新を行ってください。

実行対象と実行元の環境でインストールしたバージョンを確認するには、 **詳細バージョン情報を表示** のリンクを確認します。これは **環境の詳細** ページにあります。

**MRApplicationService** を検索し、対象となる環境が実行元の環境と同等かそれ以上のバージョンあることを確認してください。

<img src="media/FinancialReporting_Binaries2.png" width="500px" alt="MRApplicationService">

8.1またはそれ以降のバージョンを使用しているお客様
1. **更新** のタイルメニューを開き、UAT環境を更新します。 更新内容をプロジェクトの資産ライブラリに保存します。
2. このパッケージをUAT環境に適用します。
3. エラーが解決されたことを確認してください。

8.0 またはそれ以前のバージョンを使用しているお客様
1. 実行元環境の環境履歴を確認します。 具体的には、「プラットフォームおよびアプリケーションのバイナリ パッケージ」のいずれかが実行元の環境に展開されていることを確認します。対象の環境ではありませんのでご注意ください。
2. このバイナリパッケージをUAT環境に適用します。
3. エラーが解決されたことを確認してください。

### <a name="incompatible-application-versions-between-source-and-target-environments"></a>ソース環境とターゲット環境間での互換性のないアプリケーション バージョン
ソースおよびターゲット環境のアプリケーション リリースが同じでない場合は、データベースの更新プロセス (セルフサービスまたはサービス要求経由) を正常に完了できません。 これは、データ アップグレード プロセスが、更新などのデータベース移動操作によって実行されず、データ損失が発生する可能性があるためです。

新しいアプリケーション バージョンにサンドボックス UAT 環境をアップグレードする場合 (たとえば、7.3 から 8.1)、必ずアップグレードを開始する前にデータベースの更新アクションを実行してください。 サンドボックスが新しいバージョンにアップグレードされると、サンドボックス UAT 環境に古い運用環境データベースを復元することはできません。

逆に、運用環境がターゲット サンドボックスよりも新しい場合、更新前にターゲット サンドボックスをアップグレードするか、更新の実行前にそのまま割り当て解除、削除、および再展開する必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
