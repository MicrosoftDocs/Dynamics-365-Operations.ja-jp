---
title: AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード
description: このトピックでは、サンドボックス環境で Dynamics AX 2012 から Dynamics 365 for Finance and Operations にデータ アップグレードを実行する方法を説明します。
author: tariqbell
manager: AnnBe
ms.date: 06/06/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 54734bee196c734d78b367e29b02c7cea14d54ab
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537207"
---
# <a name="upgrade-from-ax-2012---data-upgrade-in-sandbox-environments"></a>AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

このタスクの出力は、サンドボックス環境で使用できるデータベースのアップグレードです。 この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2/3)、またはより高度な環境を示します。 この環境では、ビジネス ユーザーと機能チームのメンバーがアプリケーション機能を検証できます。 この機能には、カスタマイズ内容や Microsoft Dynamics AX 2012 から継承されたデータが含まれます。

この方法は、データを正常にアップグレードするのに必要な全体的な時間の短縮に役立つため、共有サンドボックス環境で実行する前に開発環境でデータ アップグレード プロセスを実行することを強くお勧めします。 詳細については、[開発環境でのデータ アップグレード](prepare-data-upgrade.md) を参照してください。

> [!NOTE]
> このプロセスを開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。[SQL Server Management Studio のダウンロード](/sql/ssms/download-sql-server-management-studio-ssms). 

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>サンドボックス データ アップグレード プロセスの概要
サンドボックス環境でのデータのアップグレードを開始する前に、[開発環境でのデータ アップグレード](prepare-data-upgrade.md) で説明しているように、開発環境で既にデータがアップグレードされています。 2 つのプロセスはよく似ています。 主な違いは、サンドボックス環境では Microsoft Azure SQL データベースをデータ保管に使用し、開発環境では Microsoft SQL Server を使用する点です。 このデータベース レイヤーの技術的な違いにより、AX 2012 データベース インスタンスからのバックアップを SQL データベースに復元できないため、サンドボックス環境でデータのアップグレード手順を少し変更する必要があります。

![サンドボックス データのアップグレード プロセス](./media/data-upgrade-sandbox.png)

アップグレード プロセスの高レベルの手順を以下に示します。

1. AX 2012 AOS インスタンスをオフにします。
2. AX 2012 データベースのコピーを作成します。 エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。
3. SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。 このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。
4. Azure ストレージに bacpac ファイルをアップロードします。
5. サンドボックス環境で bacpac ファイルを Application Object Server (AOS) コンピューターにダウンロードし、SQLPackage.exe を使用してインポートします。 SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。
6. インポートされたデータベースに対して適切なデータ アップグレード パッケージを実行します。

## <a name="turn-off-the-ax-2012-aos-instances"></a>AX 2012 AOS インスタンスをオフにします。

このタスクには、AX 2012 のシステム管理者とサーバー管理者が含まれます。

AOS インスタンスをオフにする前に、実行しているすべてのバッチ ジョブを停止する必要があります。 既に稼働し始めている実行時間の長いバッチ ジョブでは、システムが停止しないようにします。 必要な場合は AOS インスタンスを停止できるように、事前に計画してください。 AX 2012 をオフにする前にバッチが完了するよう、バッチをスケジュールする必要があります。

AX 2012 環境と統合されている他のシステムをお持ちかもしれません。 AX 2012 をオフにするための計画には、これらのシステムも考慮する必要があります。 たとえば、AX 2012 自体をオフにする前に、統合システムをしばらくオフにして、残りのインフライト トランザクションを完了する必要があります。 統合システムの要件は、企業間で広く異なります。 したがって、専門家チームはこのシナリオを個別に計画する必要があります。

## <a name="create-a-copy-of-the-ax-2012-database"></a>AX 2012 データベースのコピーの作成

データベースから一部のオブジェクトを削除する必要があるため、アップグレードを実行している AX 2012 データベースのコピーを作成する必要があります。 これらのオブジェクトには、Microsoft Windows 認証ユーザーが含まれます。 これらの変更により、変更されたデータベースは AX 2012 で使用できなくなります。 この手順では、データベースのコピーを作成してこれらのオブジェクトを削除します。

この手順は、データベース管理者 (DBA) または同様の知識と経験を持っている人物が行う必要があります。

データベースのコピーを作成するには、元のデータベースのバックアップを作成し、新しい名前で復元します。 両方のデータベースに十分なスペースがあることを確認します。 別のサーバーでコピーを作成できます。 データベースを実行する SQL Server インスタンスのバージョンは重要ではありません。

データベースのコピーを作成するコードの例を以下に示します。 特定のデータベース名を反映するよう、この例を変更する必要があります。

```
    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5
```
## <a name="run-the-t-sql-script-to-prepare-the-database"></a>データベースの準備のため T-SQL スクリプトを実行

このスクリプトは、ユーザーを削除、AX 2012 RTM モデル ストアに関連するステップを削除、スキーマをクリーンアップ、ビューを削除、および tempDB への参照を削除によってデータベースを準備します。 

コピーが作成されたら、次の Transact-SQL (T-SQL) スクリプトを実行します。

```
    --remove NT users as these are not supported in Azure SQL Database
    declare 
    @SQL varchar(255),
    @UserName varchar(255)

    set quoted_identifier off

    declare     userCursor CURSOR for
    select name from sys.sysusers where (isntuser = 1 or isntgroup =1) and name <> 'dbo'

    OPEN userCursor
        FETCH userCursor into @UserName
        WHILE @@Fetch_Status = 0
          BEGIN
            set @SQL = 'DROP USER [' + @UserName + ']'
            exec(@SQL)
            FETCH userCursor into @UserName
          END
    CLOSE userCursor
    DEALLOCATE userCursor

    go

    --remove any AX 2012 RTM model store procedures that still exist
    declare 
    @SQL varchar(255),
    @procname varchar(255)

    set quoted_identifier off

    declare     procCursor CURSOR for
    select name from sys.procedures where name like 'XI_%' or name like 'XU_%'

    OPEN procCursor
        FETCH procCursor into @procname
        WHILE @@Fetch_Status = 0
          BEGIN
            set @SQL = 'DROP PROCEDURE [' + @procname + ']'
            exec(@SQL)
            FETCH procCursor into @procname
          END
    CLOSE procCursor
    DEALLOCATE procCursor

    go

    --If you receive a message that you cannot delete users because they own a schema, then check which schema the user owns. 
    --Either change the ownership to another user (for example to dbo) or drop the schema if it does not contain any objects. 
    --The examples below are for an AX 2012 demo environment. You will need to edit this for your specific environment.

        if exists (select 1 from sys.schemas where name = 'contoso\admin')
    begin
        drop schema [contoso\admin]
    end
    if exists (select 1 from sys.schemas where name = 'contoso\Domain Users')
    begin
        drop schema [CONTOSO\Domain Users]
    end
    go

    --drop all views in the current database because some refresh the tempDB, which is not a supported action in Azure SQL Databases
    declare 
    @SQL2 varchar(255),
    @ViewName varchar(255)

    set quoted_identifier off

    declare     viewCursor CURSOR for

    select viewname = v.name
    from sys.views v
    order by v.name

    OPEN viewCursor

    FETCH viewCursor into @ViewName
        WHILE @@Fetch_Status = 0
          BEGIN
            set @SQL2 = 'DROP VIEW ' + @ViewName
            exec(@SQL2)
            FETCH viewCursor into @ViewName
          END
    CLOSE viewCursor
    DEALLOCATE viewCursor
    go

    -- Drop the following procedure because it contains a tempDB reference that is not supported in Azure SQL Database
    If exists (select 1 from sys.procedures where name = 'MaintainShipCarrierRole')
    begin
        drop procedure MaintainShipCarrierRole
    end
```

## <a name="export-the-copied-database-to-a-bacpac-file"></a>コピーしたデータベースを bacpac ファイルにエクスポートする

SQLPackage.exe ツールを使用して、コピーしたデータベースを bacpac ファイルにエクスポートします。 この手順は、DBA または同等の知識を持っているチーム メンバーが行う必要があります。

> [!IMPORTANT]
> この手順を開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。 SQLPackage は以前のバージョンの Management Studio に存在しますが、まず最新バージョンをインストールしない限り、このステップでは正しく動作しません。


この手順は重要です。稼動前のダウンタイム中にエクスポートを再度実行する必要があるためです。 いくつかのヒントを以下に示します。

- bacpac プロセスでは、I/O および CPU に非常に負荷がかかります。 したがって、高性能コンピューターでエクスポートを実行します。
- SQLPackage は、データベースをホストするコンピューターにローカルで実行する必要があります。 この処理もネットワーク集中型であるため、データベース コンピューターに接続するローカルのラップトップで SQLPackage を実行しないでください。

次に、管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

パラメータの説明を以下に示します。

- **ssn** (ソース サーバー名) – エクスポートする SQL Server の名前。 このプロセスでは、このパラメータは常に **localhost** に設定する必要があります。
- **sdn** (ソース データベース名) – エクスポートするデータベースの名前。
- **tf** (ターゲット ファイル) – エクスポートするファイルのパスと名前。 フォルダーが既に存在するはずですが、ファイルはプロセスによって作成されます。
- **/p:CommandTimeout** – クエリあたりのタイムアウト値。 このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。

## <a name="upload-the-bacpac-file-to-azure-storage-or-the-lcs-asset-library"></a>Azure ストレージまたは LCS アセット ライブラリに bacpac ファイルをアップロード

作成した bacpac ファイルは、Azure でホストされたサンドボックス環境の AOS マシンにコピーする必要があります。 これを引当するためのいくつかの理由があります。
1. レベル 2 (またはそれ以上) サンドボックス環境により使用される Azure SQL データベース インスタンスには、環境自体の外からのアクセスを防ぐファイアウォール ルールがあります。
2. Bacpac インポートのパフォーマンスは、Azure SQL データベース インスタンスとし同じ Azure データセンター コンピューターからインポートした場合、何倍も向上します。

bacpac ファイルを AOS マシンに移動する方法を選択することができます。自分の SFTP または他のセキュアな転送サービスがある可能性があります。 Azure ストレージを使用することをお勧めします。Azure ストレージを使用するには、ユーザー自身のサブスクリプション (Dynamics サブスクリプション自体に含まれていません)で独自の Azure ストレージ アカウントを取得する必要があります。 Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは [Azcopy](/azure/storage/storage-use-azcopy) を、GUI 操作からは [Microsoft Azure ストレージ エクスプローラー](http://storageexplorer.com/) を使用できます。 これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。

もう 1 つの (無料) オプションは、LCS 資産ライブラリを使用することですが、アップロードやダウンロードは Azure ストレージよりも時間がかかる場合があります。 このオプションを使用するには、次のようにします。
1. LCS でプロジェクトにログインし、アセット ライブラリに移動します。
2. データベース バックアップ タブを選択します。
3. bacpac ファイルをアップロードします。
その VM から LCS にログインして LCS アセット ライブラリからダウンロードすることにより、後から bacpac をサンドボックス AOS VM にダウンロードすることができます。

## <a name="import-the-bacpac-file-into-sql-database"></a>bacpac ファイルを SQL Database にインポートする

この手順では、エクスポートした bacpac ファイルを、サンドボックス環境で使用する SQL データベース インスタンスにインポートします。 まず、サンドボックス AOS コンピューターに Management Studio の最新バージョンをインストールする必要があります。 その後 SQLPackage.exe ツールを使用してファイルをインポートします。


SQL データベース インスタンスへのアクセスを制限するファイアウォール規則があるため、サンドボックス環境の AOS コンピューターでこれらのタスクを直接実行します。 ただし、AOS コンピューターを使用すると、アクセス許可を取得できます。

エクスポートの手順に関しては、インポートを開始する前に、Management Studio の最新バージョンが必要です。 以前のバージョンを使用している場合、この手順は機能しません。

パフォーマンス上の理由から、bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。 Azure 仮想マシン (VM) では、ドライブ D は通常、他の利用可能なディスクよりも高いパフォーマンスを持つ物理ディスクです。

管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```
    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=<Service objective>
```

パラメータの説明を以下に示します。

- **tsn** (ターゲット サーバー名) – インポートする SQL Azure サーバーの名前。 名前は LCS で確認できます。 末尾に **.database.windows.net** を付け加えます。
- **tdn** (ターゲット データベース名) – インポートするデータベースの名前。 データベースが既に存在していない必要があります。 インポート処理が作成されます。
- **sf** (ソース ファイル) – インポートするファイルのパスと名前。
- **tp** (ターゲット パスワード) – ターゲット SQL データベース インスタンスの SQL パスワード。
- **tu** (ターゲット ユーザー) – ターゲット SQL データベース インスタンスの SQL ユーザー名。 **sqladmin** を使用することをお勧めします。 LCS プロジェクトからは、このユーザーのパスワードを取得できます。
- **/p:CommandTimeout** – クエリあたりのタイムアウト値。 このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。
- **/p:DatabaseServiceObjective** - S1、P2、P4 など、データベースのパフォーマンス レベルを指定します。 パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。 Management Studio を使用して、既存のデータベースの値を確認できます。 データベースを右クリックし、**プロパティ** を選択します。

コマンドを実行すると、次の警告が表示される場合があります。 これは無視してかまいません。

![サンドボックス エラー](./media/sandbox-2.png)


## <a name="run-a-t-sql-script-to-update-the-database"></a>データベースの更新のため T-SQL スクリプトを実行
インポートされたデータベースに対して、次のスクリプトを実行します。 スクリプトでは次のアクションを実行します。

-   データベース ユーザーを再作成
-   適切な実績パラメーターを設定
-   SQL Query Store 機能の有効化

```
    CREATE USER axdeployuser FROM LOGIN axdeployuser
    EXEC sp_addrolemember 'db_owner', 'axdeployuser'

    CREATE USER axdbadmin WITH PASSWORD = 'password from lcs'
    EXEC sp_addrolemember 'db_owner', 'axdbadmin'

    CREATE USER axruntimeuser WITH PASSWORD = 'password from lcs'
    EXEC sp_addrolemember 'db_datareader', 'axruntimeuser'
    EXEC sp_addrolemember 'db_datawriter', 'axruntimeuser'

    CREATE USER axmrruntimeuser WITH PASSWORD = 'password from lcs'
    EXEC sp_addrolemember 'ReportingIntegrationUser', 'axmrruntimeuser'
    EXEC sp_addrolemember 'db_datareader', 'axmrruntimeuser'
    EXEC sp_addrolemember 'db_datawriter', 'axmrruntimeuser'

    CREATE USER axretailruntimeuser WITH PASSWORD = 'password from lcs'
    EXEC sp_addrolemember 'UsersRole', 'axretailruntimeuser'
    EXEC sp_addrolemember 'ReportUsersRole', 'axretailruntimeuser'

    CREATE USER axretaildatasyncuser WITH PASSWORD = 'password from lcs'
    EXEC sp_addrolemember 'DataSyncUsersRole', 'axretaildatasyncuser'

    ALTER DATABASE SCOPED CONFIGURATION  SET MAXDOP=2
    ALTER DATABASE SCOPED CONFIGURATION  SET LEGACY_CARDINALITY_ESTIMATION=ON
    ALTER DATABASE SCOPED CONFIGURATION  SET PARAMETER_SNIFFING= ON
    ALTER DATABASE SCOPED CONFIGURATION  SET QUERY_OPTIMIZER_HOTFIXES=OFF
    ALTER DATABASE imported-database-name SET COMPATIBILITY_LEVEL = 130;
    ALTER DATABASE imported-database-name SET QUERY_STORE = ON;
```

## <a name="run-the-data-upgrade-deployable-package"></a>データ アップグレード展開可能なパッケージを実行

最新の Finance and Operations 更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード展開可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共用資産ライブラリから最新のバイナリ更新プログラムをダウンロードします。

1. http://lcs.dynamics.com/ にサインイン
2. **共有資産ライブラリ** タイルを選択します。
3. **共有アセット** ライブラリの**アセット タイプの選択**で、**ソフトウェア配置可能パッケージ**を選択します。
4. 配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。 たとえば、AX 2012 からアップグレードする場合、パッケージ名は AX2012DataUpgrade から始まります。 アップグレードするリリースに対応するパッケージを選択します。 例: AX2012DataUpgrade-July2017。

詳細については、[開発、デモ、またはサンドボックス環境でのデータのアップグレード](upgrade-data-to-latest-update.md) を参照してください。 

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>データベースのコピーを開発環境でアップグレードする

開発環境で同じデータベースをアップグレードすることを強くお勧めします。 開発環境で利用できるデータベースのコピーを使用する場合は、アップグレードされたサンドボックス環境で検出されるバグを調査する方がはるかに簡単です。
