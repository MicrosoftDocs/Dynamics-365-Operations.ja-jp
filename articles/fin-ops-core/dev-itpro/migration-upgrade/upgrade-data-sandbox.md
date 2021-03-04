---
title: AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード
description: このトピックでは、サンドボックス環境で Microsoft Dynamics AX 2012 から Finance and Operations にデータ アップグレードを実行する方法を説明します。
author: laneswenka
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 8d0a41e64f22953ac417616ed8c34e20dbe60540
ms.sourcegitcommit: 5c2f4b715e3ee7ec869fb797d74c2c5e166d1583
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2021
ms.locfileid: "4930641"
---
# <a name="upgrade-from-ax-2012---data-upgrade-in-sandbox-environments"></a>AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

> [!NOTE]
> このトピックは段階的に廃止され、dacpac ファイル形式に基づく新しいプロセスが採用されます。 新しいプロセスの詳細については、「[AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境からデータをアップグレードするための DACPAC プロセス](upgrade-data-sandbox-dacpac.md)」を参照してください。

このタスクの出力は、サンドボックス環境で使用できるデータベースのアップグレードです。 このトピックでは、*サンドボックス* という用語は、SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2/3)、またはより高度な環境を示します。 この環境では、ビジネス ユーザーと機能チームのメンバーがアプリケーション機能を検証できます。 この機能には、カスタマイズ内容や Microsoft Dynamics AX 2012 から継承されたデータが含まれます。

この方法は、データを正常にアップグレードするのに必要な全体的な時間の短縮に役立つため、共有サンドボックス環境で実行する前に開発環境でデータ アップグレード プロセスを実行することを強くお勧めします。 詳細については[AX 2012からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト](prepare-data-upgrade.md) を参照してください。

> [!NOTE]
> このプロセスを開始する前に、SQLPackage の最新バージョンをインストールすることが非常に重要です。 これを行うには、[SQLPackage のダウンロードとインストール](/sql/tools/sqlpackage-download) を参照してください。 .NET Core バージョンの使用をお勧めします。 これは C:\temp に保存および抽出することができます。

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>サンドボックス データ アップグレード プロセスの概要
サンドボックス環境でのデータのアップグレードを開始する前に、[AX 2012 からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト](prepare-data-upgrade.md)で説明しているように、開発環境で既にデータがアップグレードされています。 2 つのプロセスはよく似ています。 主な違いは、サンドボックス環境では Microsoft Azure SQL データベースをデータ保管に使用し、開発環境では Microsoft SQL Server を使用する点です。 このデータベース レイヤーの技術的な違いにより、AX 2012 データベース インスタンスからのバックアップを SQL データベースに復元できないため、サンドボックス環境でデータのアップグレード手順を少し変更する必要があります。

![サンドボックス データのアップグレード プロセス](./media/data-upgrade-sandbox.png)

アップグレード プロセスの高レベルの手順を以下に示します。

1. AX 2012 AOS インスタンスをオフにします。
2. AX 2012 データベースのコピーを作成します。 エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。
3. SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。 このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。
4. オプションで、クラウドでホストされている VM からインポートを実行している場合は、bacpac ファイルを Azure ストレージにアップロードする必要があります。 
5. SQLPackage.exe を使用して bacpac ファイルをインポートします。 ローカル サーバーまたはクラウドでホストされている VM から実行できます。 ローカル サーバーを使用する場合は、Dynamics 365 データベースへの JIT アクセスを要求し、必要なファイアウォール ルールを設定する必要があります。 クラウドでホストされている VM を使用している場合は、bacpac ファイルをダウンロードします。 SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。

6. インポートされたデータベースに対して適切なデータ アップグレード パッケージを実行します。

## <a name="turn-off-the-ax-2012-aos-instances"></a>AX 2012 AOS インスタンスをオフにします。

このタスクには、AX 2012 のシステム管理者とサーバー管理者が含まれます。

AOS インスタンスをオフにする前に、実行しているすべてのバッチ ジョブを停止する必要があります。 既に稼働し始めている実行時間の長いバッチ ジョブでは、システムが停止しないようにします。 必要な場合は AOS インスタンスを停止できるように、事前に計画してください。 AX 2012 をオフにする前にバッチが完了するよう、バッチをスケジュールする必要があります。

AX 2012 環境と統合されている他のシステムをお持ちかもしれません。 AX 2012 をオフにするための計画には、これらのシステムも考慮する必要があります。 たとえば、AX 2012 自体をオフにする前に、統合システムをしばらくオフにして、残りのインフライト トランザクションを完了する必要があります。 統合システムの要件は、企業間で広く異なります。 したがって、専門家チームはこのシナリオを個別に計画する必要があります。

## <a name="create-a-copy-of-the-ax-2012-database"></a>AX 2012 データベースのコピーの作成

データベースから一部のオブジェクトを削除する必要があるため、アップグレードを実行している AX 2012 データベースのコピーを作成する必要があります。 これらのオブジェクトには、Microsoft Windows 認証ユーザーが含まれます。 これらの変更により、変更されたデータベースは AX 2012 で使用できなくなります。 この手順では、データベースのコピーを作成してこれらのオブジェクトを削除します。

この手順は、データベース管理者 (DBA) または同様の知識と経験を持っている人物が行う必要があります。

データベースのコピーを作成するには、元のデータベースのバックアップを作成し、新しい名前で復元します。 両方のデータベースに十分なスペースがあることを確認します。 別のサーバーでコピーを作成できます。 データベースを実行する SQL Server インスタンスのバージョンは重要ではありません。

このアクションを実行するには、ソースデータベースを右クリックし、**タスク** \> **バックアップ** を選択します。 フル コピー バックアップを作成します。 既存のデータベースのバックアップが上書きされないようにするために、ファイルを別の名前でバックアップ ディレクトリに保存することをお勧めします。

## <a name="run-the-t-sql-script-to-prepare-the-database"></a>データベースの準備のため T-SQL スクリプトを実行

このスクリプトは、ユーザーを削除、AX 2012 RTM モデル ストアに関連するステップを削除、スキーマをクリーンアップ、ビューを削除、および tempDB への参照を削除によってデータベースを準備します。 

コピーが作成されたら、次の Transact-SQL (T-SQL) スクリプトを実行します。

```sql
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

> [!NOTE]
> このトピックは段階的に廃止され、dacpac ファイル形式に基づく新しいプロセスが採用されます。 新しいプロセスの詳細については、「[AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境からデータをアップグレードするための DACPAC プロセス](upgrade-data-sandbox-dacpac.md)」を参照してください。

SQLPackage.exe ツールを使用して、コピーしたデータベースを bacpac ファイルにエクスポートします。 この手順は、DBA または同等の知識を持っているチーム メンバーが行う必要があります。

> [!IMPORTANT]
> この手順を開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。 SQLPackage は以前のバージョンの Management Studio に存在しますが、まず最新バージョンをインストールしない限り、このステップでは正しく動作しません。


この手順は重要です。稼動前のダウンタイム中にエクスポートを再度実行する必要があるためです。 いくつかのヒントを以下に示します。

- bacpac プロセスでは、I/O および CPU に非常に負荷がかかります。 したがって、高性能コンピューターでエクスポートを実行します。
- SQLPackage は、データベースをホストするコンピューターにローカルで実行する必要があります。 この処理もネットワーク集中型であるため、データベース コンピューターに接続するローカルのラップトップで SQLPackage を実行しないでください。

次に、管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```Console
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

パラメータの説明を以下に示します。

- **ssn** (ソース サーバー名) – エクスポートする SQL Server の名前。 このプロセスでは、パラメータは常に **localhost** に設定する必要があります。
- **sdn** (ソース データベース名) – エクスポートするデータベースの名前。
- **tf** (ターゲット ファイル) – エクスポートするファイルのパスと名前。 フォルダーが既に存在するはずですが、ファイルはプロセスによって作成されます。
- **/p:CommandTimeout** – クエリあたりのタイムアウト値。 このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。

## <a name="upload-the-bacpac-file-to-azure-storage-or-the-lcs-asset-library"></a>Azure ストレージまたは LCS アセット ライブラリに bacpac ファイルをアップロード

作成した bacpac ファイルは、Azure でホストされたサンドボックス環境の AOS マシンにコピーする必要があります。 これを引当するためのいくつかの理由があります。
1. レベル 2 (またはそれ以上) サンドボックス環境により使用される Azure SQL データベース インスタンスには、環境自体の外からのアクセスを防ぐファイアウォール ルールがあります。
2. Bacpac インポートのパフォーマンスは、Azure SQL データベース インスタンスとし同じ Azure データセンター コンピューターからインポートした場合、何倍も向上します。

bacpac ファイルを AOS マシンに移動する方法を選択することができます。自分の SFTP または他のセキュアな転送サービスがある可能性があります。 Azure ストレージを使用することをお勧めします。Azure ストレージを使用するには、ユーザー自身のサブスクリプション (Dynamics サブスクリプション自体に含まれていません)で独自の Azure ストレージ アカウントを取得する必要があります。 Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは [Azcopy](/azure/storage/storage-use-azcopy) を、GUI 操作からは [Microsoft Azure ストレージ エクスプローラー](https://storageexplorer.com/) を使用できます。 これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。

Microsoft Dynamics Lifecycle Services (LCS) でアセット ライブラリを使用することもできます。 ただし、アップロードとダウンロードには、Azure ストレージよりも長い時間がかかります。 このオプションを使用するには、次のようにします。
1. LCS でプロジェクトにサインインし、アセット ライブラリに移動します。
2. データベース バックアップ タブを選択します。
3. bacpac ファイルをアップロードします。
サンドボックス AOS サーバーへの RDP アクセスが削除されたため、サンドボックス環境と同じリージョンで実行されているクラウド ホスト環境を使用してファイルをインポートすることをお勧めします。 クラウドでホストされている VM に bacpac ファイルをダウンロードするには、そのコンピューターの LCS にサインインし、LCS アセット ライブラリからダウンロードします。

## <a name="import-the-bacpac-file-into-sql-database"></a>bacpac ファイルを SQL Database にインポートする

> [!NOTE]
> このトピックは段階的に廃止され、dacpac ファイル形式に基づく新しいプロセスが採用されます。 新しいプロセスの詳細については、「[AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境からデータをアップグレードするための DACPAC プロセス](upgrade-data-sandbox-dacpac.md)」を参照してください。

この手順では、エクスポートした bacpac ファイルを、サンドボックス環境で使用する SQL Server データベース インスタンスにインポートします。 上記のように、サンドボックス AOS サーバーへの RDP アクセスが削除されたため、サンドボックス環境と同じリージョンで実行されているクラウド ホスト環境を使用してファイルをインポートすることをお勧めします。 データベースへの JIT アクセスを要求し、ローカル サーバーから実行することができます。 この操作を行うには、[ジャストインタイム データベース アクセスの有効化](../database/database-just-in-time-JIT-access.md)のプロセスに従って、IP アドレスをデータベースの許可リストにします。

最初に、クラウドでホストされている VM またはローカル サーバーに Management Studio の最新バージョンをインストールする必要があります。 その後 SQLPackage.exe ツールを使用してファイルをインポートします。

クラウド ホスト環境を使用している場合は、パフォーマンス上の理由から、AOS マシンのドライブ D に bacpac ファイルを配置することをお勧めします。 Azure 仮想マシン (VM) では、ドライブ D は通常、他の利用可能なディスクよりも高いパフォーマンスを持つ物理ディスクです。

管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```Console
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tdn:<New database name> /tu:sqladmin /tp:<password from LCS> /mp:64 /p:CommandTimeout=1200 /p:DatabaseEdition=<Edition> /p:DatabaseServiceObjective=<Service objective> /p:DatabaseMaximumSize=<Maximum size>
```

パラメータの説明を以下に示します。

- **sf** (ソース ファイル) – インポートするファイルのパスと名前。
- **tsn** (ターゲット サーバー名) – インポートする SQL Azure サーバーの名前。 名前は LCS で確認できます。 末尾に **.database.windows.net** を付け加えます。
- **tdn** (ターゲット データベース名) – インポートするデータベースの名前。 データベースが既に存在していない必要があります。 インポート処理が作成されます。
- **tu** (ターゲット ユーザー) – ターゲット SQL データベース インスタンスの SQL ユーザー名。 **sqladmin** を使用することをお勧めします。 LCS プロジェクトからは、このユーザーのパスワードを取得できます。
- **tp** (ターゲット パスワード) – ターゲット SQL データベース インスタンスの SQL パスワード。
- **mp** (最大並列処理) - データベースに対して実行される同時操作の並列度を指定します。 既定値は 8 です。 値を 64 にすると、ほとんどの場合に最高のパフォーマンスが得られます。
- **/p:CommandTimeout** – クエリあたりのタイムアウト値。 このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。
- **/p:DatabaseEdition** – Basic、Standard、Premium、GeneralPurpose、BusinessCritical、Hyperscale などのデータベースのエディションを指定します。 パフォーマンス要件を満たし、サービス契約を遵守するには、この環境で現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルを使用します。 Management Studio を使用して、既存のデータベースの値を確認できます。 データベースを右クリックし、**プロパティ** を選択します。
- **/p:DatabaseServiceObjective** - S1、P2、P4 または GP_Gen5_8 など、データベースのパフォーマンス レベルを指定します。 パフォーマンス要件を満たし、サービス契約を遵守するには、この環境で現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルを使用します。 Management Studio を使用して、既存のデータベースの値を確認できます。 データベースを右クリックし、**プロパティ** を選択します。
- **/p:DatabaseMaximumSize** – Azure SQL データベースの最大サイズを GB 単位で定義します。 大きなデータベースをインポートできるようにするには、このパラメータを使用する必要があります。

コマンドを実行すると、次の警告を受け取る場合があります。 これは無視してかまいません。

![サンドボックス エラー](./media/sandbox-2.png)

無効な値に関するエラー メッセージを受け取る場合は、パラメータを再確認してください。 問題がない場合は、新しいバージョンの SqlPackage を使用する必要があります。 [Windows .NET Core](/sql/tools/sqlpackage-download) バージョンをインストールすることなく使用できます。 これは、たとえば、C:\Temp\Sqlpackage-dotnetcore に抽出できる .zip ファイルです。 これで、データベースをインポートするときに、C:\Program Files (x86) の下で Sqlpackage.exe を使用する代わりに、C:\Temp\Sqlpackage-dotnetcore で Sqlpackage.exe を使用できます。


## <a name="run-a-t-sql-script-to-update-the-database"></a>データベースの更新のため T-SQL スクリプトを実行
インポートされたデータベースに対して、次のスクリプトを実行します。 スクリプトでは次のアクションを実行します。

-   データベース ユーザーを再作成
-   適切な実績パラメーターを設定
-   SQL Query Store 機能の有効化

```sql
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

レベル 2 のサンドボックス環境では、レベル 1 の DevTest 環境と同様に、データ アップグレード パッケージを LCS から直接実行できるようになりました。 パッケージを適用するには、LCS の環境に移動し、**メンテナンス** \> **更新プログラムの適用** を選択します。 一覧の一番下までスクロールし、共用資産ライブラリからデータ アップグレード パッケージが読み込まれるまで待ちます。 パッケージが読み込まれるまでにしばらく時間がかかる場合があります。 リストにデータ アップグレード パッケージが表示されない場合は、LCS のプロジェクト設定に移動し、レガシ システムが **AX2012 アップグレード** に設定されていることを確認してください。 その後、パッケージを適用できます。

選択するパッケージの名前は、使用しているバージョンと一致している必要があります。 たとえば、バージョン 10.0.14 にアップグレードするには、**AX2012DataUpgrade-10-0-14** を選択します。

詳細については、 [開発、デモ、サンドボックス環境でのデータの更新](upgrade-data-to-latest-update.md) を参照してください。 

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>データベースのコピーを開発環境でアップグレードする

開発環境で同じデータベースをアップグレードすることを強くお勧めします。 開発環境で利用できるデータベースのコピーを使用する場合は、アップグレードされたサンドボックス環境で検出されるバグを調査する方がはるかに簡単です。
