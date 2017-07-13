---
title: "サンドボックス環境でのデータ アップグレード"
description: "このトピックでは、サンドボックス環境で AX 2012 から Dynamics 365 for Finance and Operations にデータ アップグレードを実行する方法を説明します。"
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: ja-jp
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>サンドボックス環境でのデータ アップグレード

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

このタスクの出力は、サンドボックス環境で使用できるデータベースのアップグレードです。 サンドボックス環境は、ビジネス ユーザーおよび機能チームのメンバーがアプリケーション機能を検証する環境です。 この機能には、カスタマイズ内容や Microsoft Dynamics AX 2012 から継承されたデータが含まれます。

この方法は、データを正常にアップグレードするのに必要な全体的な時間の短縮に役立つため、共有サンドボックス環境で実行する前に開発環境でデータ アップグレード プロセスを実行することを強くお勧めします。 詳細については、[開発環境でのデータ アップグレード](prepare-data-upgrade.md) を参照してください。

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>サンドボックス データ アップグレード プロセスの概要

サンドボックス環境でのデータのアップグレードを開始する前に、[開発環境でのデータ アップグレード](prepare-data-upgrade.md) で説明しているように、開発環境で既にデータがアップグレードされています。 2 つのプロセスはよく似ています。 主な違いは、サンドボックス環境では Microsoft Azure SQL データベースをデータ保管に使用し、開発環境では Microsoft SQL Server を使用する点です。 このデータベース レイヤーの技術的な違いにより、AX 2012 データベース インスタンスからのバックアップを SQL データベースに復元できないため、サンドボックス環境でデータのアップグレード手順を少し変更する必要があります。

![サンドボックス データのアップグレード プロセス](./media/data-upgrade-sandbox.png)

アップグレード プロセスの高レベルの手順を以下に示します。

1. AX 2012 データベースのコピーを作成します。 エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。
2. SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。 このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。
3. Azure ストレージに bacpac ファイルをアップロードします。
4. サンドボックス環境で bacpac ファイルを Application Object Server (AOS) コンピューターにダウンロードし、SQLPackage.exe を使用してインポートします。 SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。
5. インポートされたデータベースに対してデータのアップグレードを実行する MajorVersionDataUpgrade.zip パッケージを実行します。

## <a name="create-a-copy-of-the-ax-2012-database"></a>AX 2012 データベースのコピーを作成する

データベースから一部のオブジェクトを削除する必要があるため、アップグレードを実行している AX 2012 データベースのコピーを作成する必要があります。 これらのオブジェクトには、Microsoft Windows 認証ユーザーが含まれます。 これらの変更により、変更されたデータベースは AX 2012 で使用できなくなります。 この手順では、データベースのコピーを作成してこれらのオブジェクトを削除します。

この手順は、データベース管理者 (DBA) または同様の知識と経験を持っている人物が行う必要があります。

データベースのコピーを作成するには、元のデータベースのバックアップを作成し、新しい名前で復元します。 両方のデータベースに十分なスペースがあることを確認します。 別のサーバーでコピーを作成できます。 データベースを実行する SQL Server インスタンスのバージョンは重要ではありません。

データベースのコピーを作成するコードの例を以下に示します。 特定のデータベース名を反映するよう、この例を変更する必要があります。

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

コピーが作成されたら、次の Transact-SQL (T-SQL) スクリプトを実行します。
TODO 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>コピーしたデータベースを bacpac ファイルにエクスポートする

SQLPackage.exe ツールを使用して、コピーしたデータベースを bacpac ファイルにエクスポートします。 この手順は、DBA または同等の知識を持っているチーム メンバーが行う必要があります。

この手順を開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。 SQLPackage は以前のバージョンの Management Studio に存在しますが、まず最新バージョンをインストールしない限り、このステップでは正しく動作しません。

この手順は重要です。稼動前のダウンタイム中にエクスポートを再度実行する必要があるためです。 いくつかのヒントを以下に示します。

- bacpac プロセスでは、I/O および CPU に非常に負荷がかかります。 したがって、高性能コンピューターでエクスポートを実行します。
- SQLPackage は、データベースをホストするコンピューターにローカルで実行する必要があります。 この処理もネットワーク集中型であるため、データベース コンピューターに接続するローカルのラップトップで SQLPackage を実行しないでください。

次に、管理者として [**コマンド プロンプト**] ウィンドウを開き、次のコマンドを実行します。

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

パラメータの説明を以下に示します。

- **ssn** (ソース サーバー名) – エクスポートする SQL Server の名前。 このプロセスでは、このパラメータは常に **localhost** に設定する必要があります。
- **sdn** (ソース データベース名) – エクスポートするデータベースの名前。
- **tf** (ターゲット ファイル) – エクスポートするファイルのパスと名前。 フォルダーが既に存在するはずですが、ファイルはプロセスによって作成されます。
- **/p:CommandTimeout** – クエリあたりのタイムアウト値。 このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Azure ストレージに bacpac ファイルをアップロードする

Azure ストレージに bacpac ファイルをアップロードします。 UsingStorageExplorer.docx TODO を参照してください。

### <a name="import-the-bacpac-file-into-sql-database"></a>bacpac ファイルを SQL Database にインポートする

この手順では、エクスポートした bacpac ファイルを、サンドボックス環境で使用する SQL データベース インスタンスにインポートします。 まず、サンドボックス AOS コンピューターに Management Studio の最新バージョンをインストールする必要があります。 その後 SQLPackage.exe ツールを使用してファイルをインポートします。

SQL データベース インスタンスへのアクセスを制限するファイアウォール規則があるため、サンドボックス環境の AOS コンピューターでこれらのタスクを直接実行します。 ただし、AOS コンピューターを使用すると、アクセス許可を取得できます。

エクスポートの手順に関しては、インポートを開始する前に、Management Studio の最新バージョンが必要です。 以前のバージョンを使用している場合、この手順は機能しません。

パフォーマンス上の理由から、bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。 Azure 仮想マシン (VM) では、ドライブ D は通常、他の利用可能なディスクよりも高いパフォーマンスを持つ物理ディスクです。

管理者として [**コマンド プロンプト**] ウィンドウを開き、次のコマンドを実行します。

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

パラメータの説明を以下に示します。

- **tsn** (ターゲット サーバー名) – インポートする SQL Azure サーバーの名前。 名前は LCS で確認できます。 末尾に **.database.windows.net** を付け加えます。
- **tdn** (ターゲット データベース名) – インポートするデータベースの名前。 データベースが既に存在していない必要があります。 インポート処理が作成されます。
- **sf** (ソース ファイル) – インポートするファイルのパスと名前。
- **tp** (ターゲット パスワード) – ターゲット SQL データベース インスタンスの SQL パスワード。
- **tu** (ターゲット ユーザー) – ターゲット SQL データベース インスタンスの SQL ユーザー名。 **sqladmin** を使用することをお勧めします。 LCS プロジェクトからは、このユーザーのパスワードを取得できます。
- **/p:CommandTimeout** – クエリあたりのタイムアウト値。 このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。
- **/p:DatabaseServiceObjective** – 作成されるデータベースのサービス層レベル。 Management Studio を使用して、既存のデータベースの値を確認できます。 データベースを右クリックし、[**プロパティ**] を選択します。

コマンドを実行すると、次の警告が表示されます。 これは無視してかまいません。

![サンドボックス エラー](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>MajorVersionDataUpgrade.zip パッケージを実行する

[開発、デモ、またはサンドボックス環境でのデータのアップグレード](upgrade-data-to-latest-update.md) の説明に従って、データ アップグレードの配置可能パッケージを実行します。

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>データベースのコピーを開発環境でアップグレードする

同じデータベースを開発環境でアップグレードすると便利です。 開発環境で利用できるデータベースのコピーを使用する場合は、アップグレードされたサンドボックス環境で検出されるバグを調査する方がはるかに簡単です。

