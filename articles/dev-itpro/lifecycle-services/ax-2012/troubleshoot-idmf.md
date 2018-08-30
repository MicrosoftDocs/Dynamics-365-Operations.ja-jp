---
title: "Intelligent Data Management Framework (IDMF) のトラブルシューティング"
description: "このトピックには、Microsoft Dynamics AX Intelligent Data Management Framework (IDMF) 機能についての情報が含まれています。"
author: kfend
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18711
ms.assetid: fe0b2255-d44e-42db-9c90-2c6202fc7578
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 1ff09879a0814c0eac0c460e8e70bd6b4e1b7b17
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="troubleshoot-the-intelligent-data-management-framework-idmf"></a>Intelligent Data Management Framework (IDMF) のトラブルシューティング

[!include [banner](../../includes/banner.md)]

このトピックには、Microsoft Dynamics AX Intelligent Data Management Framework (IDMF) 機能についての情報が含まれています。

<a name="known-issues"></a>既知の問題
------------

-   **問題** サービスの設定とインストール中に提供されたドメイン アカウントには**サービスとしてログオンするためのアクセス許可**が与えられないため、IDMF サービスは開始時に失敗します。 **回避策** **サービス コントロール**パネルを開いてください。 **セキュリティ**タブで、アカウントのパスワードを入力します。
-   **問題** IDMF のサービスアカウントにローカル管理者権限が与えられていない場合、次のエラーメッセージが表示されます。未処理の例外が発生し、記録されました。 サポートにお問い合わせください。 **回避策**ローカル コンピューター上の IDMF 管理者権限にサービス アカウントを付与してください。
-   **問題** **ByFiscal** アーカイブ タスクは、メタデータ タスクの実行中にスケジュールすることはできません。 **回避策** **ByFiscal** アーカイブ タスクをスケジューリングする前にメタデータ タスクが完了するまで待ってください。
-   **問題** アーカイブの実行、オフライン **ALTER INDEX** として同時にアーカイブ タスクを削除または復元する操作により、データベースのロックに関する問題が発生します。 **回避策**アーカイブ、削除またはアーカイブ タスクの復元を実行する前に、指定されたインデックスを完了させるために**変更インデックス**操作がオフラインになるまで待ってください。
-   **問題** アーカイブ テンプレートまたは削除テンプレートは、アーカイブ タスクまたは削除タスクが実行されているときは変更しないでください。 **回避策**アーカイブまたは削除タスクが実行されているときは、アーカイブおよび削除テンプレートは変更しないでください。
-   **問題** 復元中に、バルク挿入命令を実行すると、実稼働環境の Microsoft Dynamics AX ビジネス データベースのテーブルに対して大量のテーブル ロックのエスカレーションが発生する可能性があります。 **回避策**なし。
-   **問題** **ByFiscal** タスク ページおよび他のページでは、展開と折りたたみのアイコンに逆の画像を表示することができます。 **回避策**なし。
-   **問題** ドライブ テーブルが **AccountingEvent** の場合、アーカイブ オブジェクトを検出することができません。 システムは次のメッセージを返します。「エラー実行コード: スクリプトを実行するためのメモリが不足しています」 **回避策**以下のレジストリ エントリを更新します。\[HKEY\_CURRENT\_USERSoftwareMicrosoftDynamics6.0Configurationconfiguration 名\]\[HKEY\_LOCAL\_MACHINESoftwareMicrosoftDynamics6.0Configurationconfiguration 名\]\[HKEY\_LOCAL\_MACHINESYSTEMCurrentControlSetServicesDynamics Server6.0AOS インスタンスのコンフィギュレーション名\]値の名前 :maxbuffersizeValue タイプ : レジストリ\_SZValue: メモリの最大量 (MB) または制限なしの 0

## <a name="view-log-files"></a>ログ ファイルの表示
IDMF は、エラー イベントをインストール フォルダーの下のフォルダー内のログ ファイルに記録します。 既定のインストール パスは、C:\Program File\Microsoft Dynamics AX Intelligent Data Management Framework です。 IDMF は、最初のエラー メッセージが生成されたときに、ログ ファイルを作成します。 このファイルの名前は trace\_mm-dd-yyyy.log で、mm-dd-yyyy は現在の月、日、年を示します。 IDMF スケジューラー サービスは、servicetrace\_mm-dd-yyyy.log と呼ばれるエラー ログ ファイルを作成します。 エラー ログ ファイルは、毎日作成されます。 その日に最初のエラーが発生すると、エラー ログ ファイルが作成されて、エラー メッセージが新たに作成されたエラー ログ ファイルに追加されます。 その後のすべてのエラー メッセージはその日の既存のエラー ログ ファイルに追加されます。

## <a name="database-rights-are-not-set-correctly"></a>データベース権限が正しく設定されていません
AOS サービス アカウントには、IDMF 管理データベースでの **datareader**、**datawriter**、および **ddladmin** 権限が必要です。

## <a name="idmf-fails-to-start"></a>IDMF が開始しない
IDMF を起動するときは、次のエラーが発生することがあります: 「未処理の例外が発生し、記録されました。 サポートにお問い合わせください。 上記のエラー メッセージは、エラー状態がアクセス許可などの環境問題によって発生した場合に IDMF が表示する一般的なメッセージです。 この特定のエラー状態は、通常、ユーザーに IDMF のインストール フォルダーに対する読み取りおよび書き込み許可がない場合に発生します。 エラー状態を修正するには、IDMF のインストール フォルダーに、読み取りと書き込みのアクセス許可を適用します。 既定のパスは、C:\Program Files\Microsoft Dynamics AX Intelligent Data Management Framework です。

## <a name="index-defragmentation-does-not-reduce-the-fragmentation-percentage-to-zero"></a>インデックスの最適化は最適化率をゼロまで減らしません。
インデックスの最適化スケジュールは、必ずしも完全な最適化、つまり0 (ゼロ)% の断片化を達成するとは限りません。 インデックスの一部には、引き続き小さな断片化が存在する可能性があります。 最適化プロセスは、選択されたインデックスを最大限可能なレベルまで最適化しようとします。 ただし、Microsoft Dynamics AX は、0 (ゼロ) の FILL FACTOR を使用します。 0 の FILL FACTOR は、インデックス ページを完全に埋めることなく、追加のページにレコードを分割します。 結果として、デフラグメンテーション スケジュールが正常に完了した後であっても、一部のインデックスの断片化レベルは、ゼロ以外のレベルの状態です。

## <a name="distributed-transaction-error"></a>配分トランザクション エラー
Microsoft SQL Server Integration Services (SSIS) ランタイムから次のエラーが表示される可能性があります: "エラー 0x8004D025 による分散トランザクションの OLE DB 接続を得るのに、SSIS ランタイムは失敗しました。 パートナー トランザクション マネージャーは、リモート/ネットワーク トランザクションのサポートを無効にしました。」 このエラー状態を修正するには、Microsoft 分散トランザクション コーディネーター (MSDT) 通信がファイアウォールを通過するようにサーバーを構成する必要があります。 手順については、[サポート技術情報 306843](http://support.microsoft.com/kb/306843) を参照してください。 **Microsoft 分散トランザクション コーディネーター**により、**受信および発信ルール**で**分散トランザクション コーディネーター** のファイアウォールが設定されていることを確認した後にエラーが発生する場合。

## <a name="export-to-excel-fails"></a>Excel へのエクスポートが失敗
一部の環境で Excel へのエクスポート機能が動作しない場合があります。 この問題を解決するには、Microsoft Excel と Excel PIA がコンピューターにインストールされている必要があります。 Excel が正しくインストールされ、コンピューターで動作していることを確認します。 必要に応じて、Microsoft Office プライマリ相互運用アセンブリ (PIA) をダウンロードし、インストールします。 Excel 2003 については、[Office 2003 更新プログラム: 再頒布可能パッケージのプライマリ相互運用アセンブリ](http://www.microsoft.com/downloads/details.aspx?familyid=3c9a983a-ac14-4125-8ba0-d36d67e0f4ad&displaylang=en) を参照してください。 Microsoft Excel 2007 については、[2007 Microsoft Office システム更新プログラム: 再頒布可能パッケージのプライマリ相互運用アセンブリ](http://www.microsoft.com/downloads/details.aspx?FamilyID=59daebaa-bed4-4282-a28c-b864d8bfa513&displaylang=en) を参照してください。 PIA のインストールが成功したら IDMF を再起動します。

## <a name="the-discovery-of-a-driver-table-fails"></a>ドライバー テーブルの検出に失敗します
アーカイブ オブジェクトまたは削除オブジェクトの検出プロセスを起動すると、次のエラーが発生する場合があります: 「アーカイブ オブジェクトまたは削除オブジェクトのドライバー テーブルを検出できません。」 このエラー メッセージは、通常、メタデータの同期の問題によって発生します。 このエラー状態を修正するには、インストール後のタスクを実行する必要があります。 **スタート** &gt; **すべてのプログラム** &gt; **Intelligent Data Management Framework** &gt; **インストール後の作業** をクリックしてインストール後のアプリケーションを実行するか、以下の手順に従ってこのエラーを手動で解決します。 詳細については、[Microsoft Dynamics AX インテリジェント データ管理フレームワーク (IDMF) のインストール ガイド](installation-guide-idmf.md) を参照してください。

1.  アプリケーション オブジェクト ツリー (AOT) に、**AXDataManagementToolProjectnn.xpo** が存在することを確認します。ここで nn は、Microsoft Dynamics AX アプリケーションのバージョンに応じて 50、60、61、または 62です。
2.  ポストインストール チェックリストを正常に完了したことを確認します。
3.  実装チームのすべてのメンバーが、たとえば **CUS**、**VAR**、または **USR** のように同じレイヤーで作業していることを確認します。
4.  **VAR** レイヤまたは **USR** レイヤと同じレイヤに、手順 1 に記述した XPO がインポートされていることを確認します。 これらの XPO のすべてのメソッドが、**USR** または **VAR** などの同じレイヤーにインポートされていることを確認します。
5.  AOT を使用して、AOT と、IDMF に含まれている XPO との違いを修正します。 [データ管理フレームワークのインストール ガイド](http://go.microsoft.com/fwlink/?LinkId=143616&clcid=0x409) で説明されているように、これらの XPO を現在作業中のレイヤーから削除して、手動で他のレイヤーにインポートすることができます。

## <a name="the-database-snapshot-schedule-fails-with-a-permission-error"></a>アクセス許可のエラーでデータベースのスナップショット スケジュールが失敗します
分散型 SQL Server 2008 環境では、複数のサーバーにデータベースを格納する場合、すべての SQL Server インスタンスで Service Pack 2 以降のバージョンをインストールする必要があります。 たとえば、生産データベースおよびアーカイブ データベースを 2 つの別々のサーバーに保存するときに、配分済 SQL Server 環境があります。 IDMF をインストールして開始する前に、両方のサーバーには SQL Server 2008 またはそれ以降のバージョンが必要です。 実行しないと、データベース スナップショット スケジュールから次のエラー メッセージが表示されます。「構文エラー、アクセス許可違反、またはその他の一般的なエラー」

## <a name="the-discovery-process-fails-with-an-error-message"></a>検出プロセスが失敗し、エラー メッセージが表示されます
検出プロセスで、「アーカイブ オブジェクトを作成できないか、オブジェクトを削除できません」というエラーメッセージが表示されることがあります。 このメッセージは、Application Object Server (AOS) が使用できない場合、または AOS との接続が失敗した場合に表示されることがあります。 AOS の有効性を確認してください。 必要に応じて AOS を再起動し、IDMF を再起動します。

## <a name="application-object-server-error-when-connecting-to-the-archive-database"></a>アーカイブ データベースに接続するときの Application Object Server エラー
一部の環境では、Application Object Server (AOS) がアーカイブ データベースに接続するとき、「ユーザーのセッションを作成中に内部エラーが発生しました」というエラーを受け取ることがあります。 AOS サービスに使用されるアカウントにアーカイブ データベースへの十分なアクセス許可があることを確認します。 詳細については、[データ管理フレームワークのインストール ガイド](http://go.microsoft.com/fwlink/?LinkId=143616&clcid=0x409) の「インストールに必要な権限」セクションを参照してください。 AOS サービスに使用されるアカウントがアーカイブ データベースの **CREATESERVERSESSIONS** および **CREATEUSERSESSIONS** のストアド プロシージャに対する実行権限を持っていることを確認にします。

## <a name="the-analysis-snapshot-schedule-fails-with-a-permission-error"></a>アクセス許可のエラーで分析スナップショット スケジュールが失敗します
分析スナップショット スケジュールが失敗して、エラー メッセージ「OLE DB エラーが発生しました。」が表示されます。 エラー コード: 0x80040E14.An OLE DB レコードは使用できます。 ソース: "Microsoft SQL ネイティブ クライアント" Hresult: 0x80040E14 説明: "ユーザーには、この操作を実行するためのアクセス許可がありません"。"データベースのアクセス許可の不足が原因でこのエラー メッセージが表示されます。 [データ管理フレームワークのインストール ガイド](http://go.microsoft.com/fwlink/?LinkId=143616&clcid=0x409)セクションの「インストールに必要な権限」の手順に従って、データベースのアクセス権が割り当てられていることを確認します。

## <a name="the-analysis-snapshot-schedule-fails-because-of-a-sql-server-integration-services-error"></a>分析スナップショット スケジュールは、SQL Server Integration Services のエラーが原因で失敗します
分析スナップショット スケジュールが失敗して、エラー メッセージ「メッセージ: パッケージ エラー: ファイルが存在します。」が表示されます。 バッファマネージャーが一時ファイル名を取得できませんでした。 GetTempFileName の呼び出しに失敗しました。 バッファマネージャーは、パス C:\DOCUME~1\ADMINI~1.SAMLOCALS~1Tempに一時ファイルを作成できませんでした。 パスは一時的な記憶域に対して再度は考慮されません。」 このエラーを解決するには、SQL Server 2008 以降のバージョンをインストールする必要があります。 詳細については、Microsoft サポート技術情報の記事 [972365](http://support.microsoft.com/kb/972365) を参照してください。

## <a name="unable-to-create-an-archive-schedule-or-restore-schedule"></a>アーカイブ スケジュールまたは復元スケジュールを作成できません
アーカイブ スケジュールが失敗または中止した場合は、同一のオブジェクトで別のスケジュールを作成する前に、そのスケジュールを再起動または元に戻します。 この制限は、すべてのアーカイブ オブジェクトに適用されます。

## <a name="unable-to-select-an-archive-schedule-for-restoration"></a>復元のためのアーカイブ スケジュールを選択できません
復元しようとするアーカイブ スケジュールが無効である場合があるため、選択できません。 これは、前回のスケジュールの復元が中止または失敗した場合に発生します。 ステータス ウィンドウで、中止または失敗した復元スケジュールに移動します。 スケジュールを右クリックし、実行する必要があるアクションで **スケジュールの再起動** または **スケジュールを元に戻す** を選択します。 初期化状態のときにスケジュールに失敗した場合、データがアーカイブされません。 その場合、スケジュールを復元したり戻したりする必要はなく、IDMF が新しいスケジュールを作成するよう求める警告を表示します。 **スケジュール** メニューを使用して、新しいアーカイブ スケジュールを作成します。

| **メモ**                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------|
| 常に同じアーカイブ オブジェクトに対して新しいアーカイブ スケジュールを作成する前に失敗したアーカイブ スケジュールを再起動または元に戻すことができます。 |

## <a name="a-schedule-fails-because-of-insufficient-space"></a>領域の不足が原因でスケジュールが失敗する
データベースまたはログ ファイルがいっぱいになった場合、アーカイブおよびパージ スケジュールは失敗します。 これらのスケジュールには、アーカイブまたは削除するデータの量に応じて、大量の空きデータベースとログ領域が必要です。 既定では、削除およびアーカイブ スケジュールはバッチ内の 100,000 レコードを処理します。 バッチ サイズを小さくして、スケジュールがバッチを処理するときに必要なデータベースとログ領域を減らします。 バッチ サイズをコンフィギュレーションするには、次の手順に従います。
1.  メモ帳を使用して、IDMF のインストール フォルダーから **AXDataManagementSchedulerService.exe.config** を開きます。 インストール フォルダーの既定のパスは、C:\Program Files\Microsoft Dynamics AX Intelligent Data Management Framework です。
2.  アーカイブ タスクのバッチ サイズを小さくするには、構成キー BatchSizeForPurge &lt;add key="BatchSizeForArchive" value="4000" /&gt; を見つけて、キーの値を小さい値に変更します。
3.  パージ スケジュールのバッチ サイズを小さくするには、構成キー BatchSizeForPurge &lt;add key="BatchSizeForPurge" value="4000" /&gt; を見つけて、キーの値を小さい値に変更します。

アーカイブ、生産、管理、および生産複製データベースのデータとログ ファイルの場所と初期サイズを慎重に決定する必要があります。 最適なパフォーマンスと将来の拡大に初期サイズが十分であることを確認します。 データベース の詳細については、[Microsoft Dynamics AX のデータベース コンフィギュレーションの計画](http://www.microsoft.com/downloads/details.aspx?FamilyID=ab4cd401-b366-4c1c-9a73-88c945ae8191) および Microsoft Dynamics AX のパフォーマンス チームの [ブログ](http://blogs.msdn.com/axperf/) を参照してください。

## <a name="troubleshoot-failed-schedules"></a>失敗したスケジュールのトラブルシューティング
失敗したスケジュールのトラブルシューティングを行うには、これらの手順に従います。
1.  ログ ファイル、および前のセクションで説明されている一般的な原因と関連付けられているソリューションの一覧を表示します。
2.  メタデータ同期スケジュールを経由して、生産データベースのメタデータ変更をアーカイブ データベースと同期させてください。 2 つのデータベース間でメタデータが同期されていないと、マスター データ同期スケジュールが失敗することがあります。
3.  Microsoft Distributed Transaction Coordinator (MSDTC) が正しく構成されていないと、削除スケジュールが失敗する場合があります。
4.  スケジュールは、データベースのデータ ファイルまたはログ ファイルがいっぱいになった場合に失敗することがあります。

スケジュールを再度実行する前に、エラー状態を修正する必要があります。






