---
title: AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境でデータをアップグレードするための DACPAC プロセス
description: このトピックでは、Microsoft Dynamics AX 2012 から Finance and Operations アプリにアップグレードする際に、リモート デスクトップ プロトコル (RDP) を使用してレベル 2 からレベル 5 のサンドボックス環境にアクセスできなくなった顧客に役立ちます。
author: laneswenka
manager: AnnBe
ms.date: 10/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 2a82765d0058f78e90853c6c71e6470c1405f2c7
ms.sourcegitcommit: 42dbebced4a99dfe703689b7e38c3c5caecd12e1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949239"
---
# <a name="upgrade-from-ax-2012---dacpac-process-to-upgrade-data-in-sandbox-tiers-2-5-environments"></a>AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境でデータをアップグレードするための DACPAC プロセス

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 から Finance and Operations アプリにアップグレードする際に、リモート デスクトップ プロトコル (RDP) を使用してレベル 2 からレベル 5 のサンドボックス環境にアクセスできなくなった顧客に役立つプロセス ガイドです。 データ層アプリケーション パッケージ (DACPAC) に基づく新しいファイル形式と[データベース移動ツールキット](../database/database-movement-toolkit.md) を使用することで、AX 2012 のスキーマとデータをサンドボックス環境の既存の空のデータベースに取り込むことができます。

共有サンドボックス環境で実行する前に、開発環境でデータ アップグレード プロセスを実行することを**強くお勧め**します。 この方法を使用すると、データを正常にアップグレードするために必要な時間全体を削減することができます。 詳細については[AX 2012からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト](prepare-data-upgrade.md) を参照してください。

このプロセス ガイドでは、次の手順を実行する方法について説明します。

> [!div class="checklist"]
> * サンドボックス環境データベースへのファイアウォールのアクセスを開放します。
> * すべてのオブジェクトのサンドボックス データベースを消去します。
> * スキーマを AX 2012 データベースからサンドボックス データベースに発行します。
> * データをソース データベースからターゲット データベースに転送します。
> * Microsoft Dynamics Lifecycle Services (LCS) からデータ アップグレード パッケージを適用します。
> * モック Go-Live 検証と実際の Go-Live で実稼働環境にデータベースをコピーします。

## <a name="open-firewall-access-to-your-sandbox-environment-database"></a>サンドボックス環境データベースへのファイアウォールのアクセスを開放する

既定では、すべてのサンドボックス標準受け入れテスト環境でデータベース プラットフォームとして Azure SQL データベースを使用します。 このような環境のデータベースは、最初に配置された Application Object Server (AOS) へのアクセスを制限するファイアウォールによって保護されています。

ただし、パブリック IP アドレスを使用して、ソース システムへのアクセスを許可することができます。 環境タイプと RDP アクセスに応じて、さまざまな方法でこのアクセス権を付与できます。 方法に関係なく、データベースに接続するには、サーバーとデータベースを明示的に指定する必要があります。 この情報については、LCS の環境の詳細ページを参照してください。 

ユーザー名レコード **axdbadmin** を検索して、**spartan-nam-opsprod365433\\DBOpsProd365_SandboxUAT_d2145fe** のような **{sqlServer\\sqlDatabase}** フォーマットでサーバーとデータベースを記録しておきます。 この場合、Microsoft SQL Server Management Studio (SSMS) のサーバー値は **spartan-nam-opsprod365433.database.windows.net**、データベースの値は **DBOpsProd365_SandboxUAT_d2145fe**です。 データベースを指定するには、SSMS の接続ダイアログ ボックスの**オプション**を選択する必要があります。 **axdbadmin** の資格情報 (ユーザー名とパスワード) を使用します。

### <a name="microsoft-managed-environments-where-rdp-access-is-available"></a>RDP アクセスが利用可能な Microsoft が管理する環境

サンドボックスへの RDP アクセスがある場合は、サンドボックス AOS 仮想マシン (VM) にサインインして、SSMS を開きます。 SSMS で、サーバー、ユーザー名、およびパスワードを入力します。 **オプション** タブで、LCS の **axdbadmin** レコードから明示的にデータベース名を入力します。

接続したら、データベースに対してクエリを開き、次の Transact-SQL (T-SQL) コマンドで IP アドレスを入力します。

```sql
-- Create database-level firewall setting for IP a.b.c.d 
EXECUTE sp_set_database_firewall_rule N'AX 2012 Upgrade via RDP', 'a.b.c.d', 'a.b.c.d'; 
```

ソース環境に戻って SSMS を開き、ユーザー受け入れテスト (UAT) データベースに対して同じ **axdbadmin** 資格情報を使用して接続を試みます。 次の手順に進む前に接続できることを確認する必要があります。

ファイアウォール ルールは、データベースを更新するとき、または LCS からデータベースをインポートするときに削除されることに注意してください。

### <a name="microsoft-managed-environments-without-rdp-access"></a>RDP へのアクセスがない Microsoft が管理する環境

サンドボックスへの RDP アクセスがない場合は、ご利用の IP アドレスを LCS からセルフサービス方式で許可リストに追加できます。 LCS で、サンドボックス環境の環境の詳細ページを開いて、**メンテナンス** > **アクセスの有効化**を選択してから、ダイアログ ボックスでソース環境の IP アドレスを追加します。 このエントリは数時間後に期限切れになります。

エントリが期限切れになる前に、サーバー、ユーザー名、およびパスワードを入力してサンドボックス データベースに接続します。 **オプション** タブで、LCS の **axdbadmin** レコードから明示的にデータベース名を入力します。

接続したら、データベースに対してクエリを開き、次の Transact-SQL (T-SQL) コマンドで IP アドレスを入力します。

```sql
-- Create database-level firewall setting for IP a.b.c.d 
EXECUTE sp_set_database_firewall_rule N'AX 2012 Upgrade without RDP', 'a.b.c.d', 'a.b.c.d'; 
```

ファイアウォール ルールに 2 番目のエントリが作成されます。 このエントリは期限切れになりません。 これらのファイアウォール ルールは、データベースを更新するとき、または LCS からデータベースをインポートするときに削除されることに注意してください。

### <a name="self-service-environments"></a>セルフサービス環境

AX 2012 のアップグレード シナリオでは、サンドボックス環境はサポートされていません。これは、サンドボックス環境では現在、データ アップグレード パッケージがサポートされていないためです。 Microsoft は、このサポートの追加に取り組んでおり、詳細情報が得られ次第、このトピックを更新します。

## <a name="clear-the-sandbox-database-of-all-objects"></a>すべてのオブジェクトのサンドボックス データベースを消去する

この手順では、Finance and Operations スキーマを含むサンドボックス データベースをクリーンアップします。 このプロセスにより、ソース AX 2012 スキーマを取り込むことができる空のデータベースが提供されます。 後で、そのデータベースからデータを取り込むこともできます。 データのアップグレードに失敗した場合は、いつでもこのステップに戻って最初からやり直すことができます。

SSMS を開き、前の手順と同様にサンドボックス データベースに接続します。 データベース名を右クリックして、**スクリプトの生成**を選択します。 **概要**ページで、**次へ**を選択します。 **オブジェクトの選択**ページで、**特定のデータベース オブジェクトを選択する**オプションを選択してから、次のチェック ボックスを選択します。

* テーブル
* ビュー
* ストアド プロシージャ
* ユーザー定義の関数
* スキーマ
* フル テキストのカタログ
* ユーザー定義のテーブル タイプ

**スクリプティング オプションの設定**ページで、**詳細**を選択してから、**DROP および CREATE のスクリプト**の値を **DROP のスクリプト**に変更します。 **OK** を選択してから、**新しいクエリ ウィンドウに保存**オプションを選択します。 **次へ**を選択して概要へ移動します。 表示されるクエリ ウィンドウには、オブジェクトをデータベースから削除できるように、すべてのオブジェクトを正しい順序で一覧表示するスクリプトが含まれています。

続行する準備ができたら、サンドボックス環境の AXDB データベースに対して直接生成されたクエリ ウィンドウでスクリプトを実行します。 このスクリプトを実行するには、平均 15 ~ 20 分かかります。

## <a name="publish-the-schema-from-ax-2012-to-the-sandbox-database"></a>スキーマを AX 2012 からサンドボックス データベースに発行する

データベースが空になったため、アップグレードされていない 2012 スキーマを発行できます。 このステップでは、最新バージョンの[データベース移動ツールキット](../database/database-movement-toolkit.md) をソース環境にダウンロードする必要があります。

Windows PowerShell tを使用して、データベース移動ツールキット (たとえば、C:\\dbmovement-toolkit\\) を展開したフォルダーの場所にディレクトリを変更します。 その後、**AX2012SchemaPublish.ps1** スクリプトを実行します。 次のパラメーターを使用します。

* **SourceServerName** – ソース AX 2012 データベースがホストされる場所。 この場所は **localhost** にすることができます。
* **AX2012DBName** – AX 2012 データベースの名前 (たとえば、**MicrosoftDynamicsAX**)。
* **TargetServerName** – サンドボックス データベース サーバーのサーバー値 (たとえば、**spartan-srv-12345.database.windows.net**)。 前のステップでこの値を取得しています。
* **TargetDBName** – AXDB データベースの名前 (たとえば、**d365opsprod-12345**)。 前のステップでこの値を取得しています。
* **AxDBAdminPassword** – **axdbadmin** データベース アカウントのパスワード。

![AX2012SchemaPublish.ps1 スクリプトの実行中](media/upgrade-dacpac-extract.png)

実行中、スクリプトは SqlPackage.exe を使用して、AX 2012 データベースからデータベースとスキーマの定義のみを 2012DBSource.dacpac ファイルとして作業ディレクトリに抽出します。 次に、データベース移動ツールキットに含まれている Profile.publish.xml 発行プロファイルを使用して、このファイルをサンドボックス環境に発行します。 この発行プロファイルでは、アップグレードに必要のない、SQL ビュー、SQL ユーザー、統計情報などのいくつかのオブジェクトの種類がスキップされます。

スクリプトの実行が完了したら、SSMS を開いて、サンドボックス データベースにテーブルが表示されていることを確認します。 また、テーブルが空であり、データがないことを確認します。

> [!NOTE]
> エラーのために最初からやり直す必要がある場合は、「[すべてのオブジェクトのサンドボックス データベースを消去する](#clear-the-sandbox-database-of-all-objects)」のステップに戻ります。

## <a name="transfer-data-from-ax-2012-to-the-sandbox-database"></a>AX 2012 からサンドボックス データベースにデータを転送する

スキーマの配置が完了したら、データをターゲッ トテーブルに転送する必要があります。 この転送には、SQL にリンクされているサーバーが使用されます。 転送では、データベース移動ツールキットに含まれている Windows PowerShell バージョン 7.0 以降のインスタンスで使用可能な並列処理機能も利用されます。

Windows PowerShell tを使用して、データベース移動ツールキット (たとえば、C:\\dbmovement-toolkit\\) を展開したフォルダーの場所にディレクトリを変更します。 その後、**AX2012DataTransfer.ps1** スクリプトを実行します。 次のパラメーターを使用します。

* **SourceServerName** – ソース AX 2012 データベースがホストされる場所。 この場所は **localhost** にすることができます。
* **AX2012DBName** – AX 2012 データベースの名前 (たとえば、**MicrosoftDynamicsAX**)。
* **TargetServerName** – サンドボックス データベース サーバーのサーバー値 (たとえば、**spartan-srv-12345.database.windows.net**)。 前のステップでこの値を取得しています。
* **TargetDBName** – AXDB データベースの名前 (たとえば、d365opsprod-12345)。 前のステップでこの値を取得しています。
* **AxDBAdminPassword** – axdbadmin データベース アカウントのパスワード。
* **LinkedServerName** – 作成する SQL にリンクされているサーバーの名前 (たとえば、**AX2012Link**)。
* **DegreeOfParallelism** – 並列処理する必要があるテーブルの数 (たとえば、**3**)。 このスクリプトは CPU および RAM に非常に負荷がかかるため、この値はソース環境で使用できるコアの数の半分以下である必要があります。

![AX2012DataTransfer.ps1 スクリプトを実行中](media/upgrade-dacpac-xfer.png)

実行中に、ソース サーバーとサンドボックス サーバー間のリンクされているサーバーがまだ存在していない場合は、スクリプトによって作成されます。 次に、すべての AX 2012 テーブルのデータをターゲット データベースにコピーします。 **DegreeOfParallelism** パラメーターを使用して、同時複数のテーブルを処理します。

> [!NOTE]
> エラーのために最初からやり直す必要がある場合は、「[すべてのオブジェクトのサンドボックス データベースを消去する](#clear-the-sandbox-database-of-all-objects)」のステップに戻ります。

## <a name="apply-the-data-upgrade-package-from-lcs"></a>LCS からデータ アップグレード パッケージを適用する

スキーマとデータがサンドボックス環境に移動されたので、データ アップグレード プロセスを開始できます。 前提条件として、LCS プロジェクトが AX 2012 アップグレード用に構成されていることを確認してください。 詳細については、「[AX 2012 のアップグレードとしてプロジェクトを認識する](upgrade-overview-2012.md#identify-the-project-as-an-ax-2012-upgrade)」を参照してください。

環境の環境の詳細ページで、**メンテナンス** \> **更新プログラムの適用**を選択して、読み込まれるパッケージの一覧が表示されるまで待ちます。 一覧の一番下までスクロールすると、共有アセット ライブラリから取得されたデータ アップグレード パッケージが一覧に追加されたことを確認できます。 すべての利用可能なアップグレード パッケージが読み込まれるまでにしばらく時間がかかる場合があります。

アップグレード先となるバージョンに一致するアップグレード パッケージを選択します。 たとえば、バージョン 10.0.14 にアップグレードするには、**AX2012DataUpgrade-10-0-14** を選択します。

### <a name="troubleshooting-data-upgrade-errors"></a>データ アップグレードのエラーに関するトラブルシューティング

データ アップグレードのエラーをトラブルシューティングするには、いくつかの方法があります。 場合によっては、LCS から配置可能パッケージ ログのエラーを表示できます。 たとえば、エラーがサービスの開始と停止およびデータベースの同期に関連している場合は、この方法を使用できます。

アップグレード スクリプトの実行中にアップグレードに失敗した場合は、サンドボックス データベースの ReleaseUpdateScriptsErrorLog テーブルにエラーが表示されます。 このテーブルにアクセスするには、前の手順の情報を使用してサンドボックス データベースに接続します。

データを修正できる場合は、LCS からのアップグレードを再開できます。 ただし、LCS からは 8 回を超えると再開できないことに注意してください。 サービス システムではそれ以上の試行が許可されないため、8 回以上再開しようとすると別のエラーが発生します。 この場合は、**中止**ボタンを使用してアップグレード パッケージをキャンセルし、後でもう一度やり直すことができます。

> [!NOTE]
> エラーのために最初からやり直す必要がある場合は、「[すべてのオブジェクトのサンドボックス データベースを消去する](#clear-the-sandbox-database-of-all-objects)」のステップに戻ります。

## <a name="copy-the-database-to-production-for-mock-go-live-and-actual-go-live"></a>モック Go-Live と実際の Go-Live で実稼働環境にデータベースをコピーする

データのアップグレードが完了したら、サンドボックス環境の同じカスタマイズ パッケージを実稼働環境に適用します。 その後、サンドボックス環境の AXDB データベースを実稼働環境にコピーすることができます。

コピー操作の実行方法については、「[サンドボックス データベースを実稼働環境にコピーする](../database/dbmovement-scenario-goldenconfig.md#copy-the-sandbox-database-to-production)」を参照してください。