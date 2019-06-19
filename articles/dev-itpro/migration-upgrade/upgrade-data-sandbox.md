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
ms.openlocfilehash: bfa2b12898b05691ca16e9d72f05932f33691c44
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595576"
---
# <a name="upgrade-from-ax-2012---data-upgrade-in-sandbox-environments"></a><span data-ttu-id="7425f-103">AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード</span><span class="sxs-lookup"><span data-stu-id="7425f-103">Upgrade from AX 2012 - Data upgrade in sandbox environments</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="7425f-104">このタスクの出力は、サンドボックス環境で使用できるデータベースのアップグレードです。</span><span class="sxs-lookup"><span data-stu-id="7425f-104">The output of this task is an upgraded database that you can use in a sandbox environment.</span></span> <span data-ttu-id="7425f-105">この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2/3)、またはより高度な環境を示します。</span><span class="sxs-lookup"><span data-stu-id="7425f-105">In this article, we use the term *sandbox* to refer to a Standard or Premier Acceptance Testing (Tier 2/3) or higher environment connected to a SQL Azure database.</span></span> <span data-ttu-id="7425f-106">この環境では、ビジネス ユーザーと機能チームのメンバーがアプリケーション機能を検証できます。</span><span class="sxs-lookup"><span data-stu-id="7425f-106">On this environment business users and functional team members can validate application functionality.</span></span> <span data-ttu-id="7425f-107">この機能には、カスタマイズ内容や Microsoft Dynamics AX 2012 から継承されたデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7425f-107">This functionality includes customizations and the data that was brought forward from Microsoft Dynamics AX 2012.</span></span>

<span data-ttu-id="7425f-108">この方法は、データを正常にアップグレードするのに必要な全体的な時間の短縮に役立つため、共有サンドボックス環境で実行する前に開発環境でデータ アップグレード プロセスを実行することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7425f-108">We strongly recommend that you run the data upgrade process in a development environment before you run it in a shared sandbox environment, because this approach will help reduce the overall time that is required for a successful data upgrade.</span></span> <span data-ttu-id="7425f-109">詳細については、[開発環境でのデータ アップグレード](prepare-data-upgrade.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7425f-109">For more information, see [Data upgrade in a development environment](prepare-data-upgrade.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7425f-110">このプロセスを開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。[SQL Server Management Studio のダウンロード](/sql/ssms/download-sql-server-management-studio-ssms).</span><span class="sxs-lookup"><span data-stu-id="7425f-110">It's very important that you install the latest version of SQL Server Management Studio before you start this process: [Download SQL Server Management Studio](/sql/ssms/download-sql-server-management-studio-ssms).</span></span> 

## <a name="overview-of-the-sandbox-data-upgrade-process"></a><span data-ttu-id="7425f-111">サンドボックス データ アップグレード プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="7425f-111">Overview of the sandbox data upgrade process</span></span>
<span data-ttu-id="7425f-112">サンドボックス環境でのデータのアップグレードを開始する前に、[開発環境でのデータ アップグレード](prepare-data-upgrade.md) で説明しているように、開発環境で既にデータがアップグレードされています。</span><span class="sxs-lookup"><span data-stu-id="7425f-112">Before you start to upgrade data in a sandbox environment, you will have already upgraded data in a development environment, as explained in [Data upgrade in a development environment](prepare-data-upgrade.md).</span></span> <span data-ttu-id="7425f-113">2 つのプロセスはよく似ています。</span><span class="sxs-lookup"><span data-stu-id="7425f-113">The two processes are very similar.</span></span> <span data-ttu-id="7425f-114">主な違いは、サンドボックス環境では Microsoft Azure SQL データベースをデータ保管に使用し、開発環境では Microsoft SQL Server を使用する点です。</span><span class="sxs-lookup"><span data-stu-id="7425f-114">The main difference is that a sandbox environment uses Microsoft Azure SQL Database for data storage, whereas a development environment uses Microsoft SQL Server.</span></span> <span data-ttu-id="7425f-115">このデータベース レイヤーの技術的な違いにより、AX 2012 データベース インスタンスからのバックアップを SQL データベースに復元できないため、サンドボックス環境でデータのアップグレード手順を少し変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-115">This technical difference in the database layer requires that you  modify the data upgrade procedure slightly in a sandbox environment, because a backup from the AX 2012 database instance can't just be restored to SQL Database.</span></span>

![サンドボックス データのアップグレード プロセス](./media/data-upgrade-sandbox.png)

<span data-ttu-id="7425f-117">アップグレード プロセスの高レベルの手順を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7425f-117">Here are the high-level steps in the upgrade process.</span></span>

1. <span data-ttu-id="7425f-118">AX 2012 AOS インスタンスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="7425f-118">Turn off the AX 2012 AOS instances.</span></span>
2. <span data-ttu-id="7425f-119">AX 2012 データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7425f-119">Create a copy of the AX 2012 database.</span></span> <span data-ttu-id="7425f-120">エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7425f-120">We strongly recommend that you use a copy, because you must delete some objects in the copy that will be exported.</span></span>
3. <span data-ttu-id="7425f-121">SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7425f-121">Export the copied database to a bacpac file by using a free SQL Server tool that is named SQLPackage.exe.</span></span> <span data-ttu-id="7425f-122">このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。</span><span class="sxs-lookup"><span data-stu-id="7425f-122">This tool provides a special type of database backup that can be imported into SQL Database.</span></span>
4. <span data-ttu-id="7425f-123">Azure ストレージに bacpac ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="7425f-123">Upload the bacpac file to Azure storage.</span></span>
5. <span data-ttu-id="7425f-124">サンドボックス環境で bacpac ファイルを Application Object Server (AOS) コンピューターにダウンロードし、SQLPackage.exe を使用してインポートします。</span><span class="sxs-lookup"><span data-stu-id="7425f-124">Download the bacpac file to the Application Object Server (AOS) machine in the sandbox environment, and then import it by using SQLPackage.exe.</span></span> <span data-ttu-id="7425f-125">SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-125">You must then run a script against the imported database to reset the SQL database users.</span></span>
6. <span data-ttu-id="7425f-126">インポートされたデータベースに対して適切なデータ アップグレード パッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-126">Run the appropriate data upgrade package against the imported database.</span></span>

## <a name="turn-off-the-ax-2012-aos-instances"></a><span data-ttu-id="7425f-127">AX 2012 AOS インスタンスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="7425f-127">Turn off the AX 2012 AOS instances</span></span>

<span data-ttu-id="7425f-128">このタスクには、AX 2012 のシステム管理者とサーバー管理者が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7425f-128">This task involves the AX 2012 system administrator and the server administrators.</span></span>

<span data-ttu-id="7425f-129">AOS インスタンスをオフにする前に、実行しているすべてのバッチ ジョブを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-129">Before you turn off AOS instances, you must stop all batch jobs that are running.</span></span> <span data-ttu-id="7425f-130">既に稼働し始めている実行時間の長いバッチ ジョブでは、システムが停止しないようにします。</span><span class="sxs-lookup"><span data-stu-id="7425f-130">A long-running batch job that has already started to run will prevent the system from stopping.</span></span> <span data-ttu-id="7425f-131">必要な場合は AOS インスタンスを停止できるように、事前に計画してください。</span><span class="sxs-lookup"><span data-stu-id="7425f-131">Plan ahead, so that you can stop your AOS instances when needed.</span></span> <span data-ttu-id="7425f-132">AX 2012 をオフにする前にバッチが完了するよう、バッチをスケジュールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-132">You might have to schedule batches so that they're completed some time before you turn off AX 2012.</span></span>

<span data-ttu-id="7425f-133">AX 2012 環境と統合されている他のシステムをお持ちかもしれません。</span><span class="sxs-lookup"><span data-stu-id="7425f-133">You might have other systems that are integrated with the AX 2012 environment.</span></span> <span data-ttu-id="7425f-134">AX 2012 をオフにするための計画には、これらのシステムも考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-134">You must also factor these systems into your plan to turn off AX 2012.</span></span> <span data-ttu-id="7425f-135">たとえば、AX 2012 自体をオフにする前に、統合システムをしばらくオフにして、残りのインフライト トランザクションを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-135">For example, you might have to turn off the integrated systems some time before you turn off AX 2012 itself, so that any remaining in-flight transactions can be completed.</span></span> <span data-ttu-id="7425f-136">統合システムの要件は、企業間で広く異なります。</span><span class="sxs-lookup"><span data-stu-id="7425f-136">The requirements for integrated systems vary widely from business to business.</span></span> <span data-ttu-id="7425f-137">したがって、専門家チームはこのシナリオを個別に計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-137">Therefore, your team of experts must plan for this scenario independently.</span></span>

## <a name="create-a-copy-of-the-ax-2012-database"></a><span data-ttu-id="7425f-138">AX 2012 データベースのコピーの作成</span><span class="sxs-lookup"><span data-stu-id="7425f-138">Create a copy of the AX 2012 database</span></span>

<span data-ttu-id="7425f-139">データベースから一部のオブジェクトを削除する必要があるため、アップグレードを実行している AX 2012 データベースのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-139">You must create a copy of the AX 2012 database that you're upgrading, because you must delete some objects from the database.</span></span> <span data-ttu-id="7425f-140">これらのオブジェクトには、Microsoft Windows 認証ユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7425f-140">These objects include any Microsoft Windows authentication users.</span></span> <span data-ttu-id="7425f-141">これらの変更により、変更されたデータベースは AX 2012 で使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="7425f-141">These changes make the modified database unusable for AX 2012.</span></span> <span data-ttu-id="7425f-142">この手順では、データベースのコピーを作成してこれらのオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="7425f-142">During this step, you will create a copy of the database and delete these objects.</span></span>

<span data-ttu-id="7425f-143">この手順は、データベース管理者 (DBA) または同様の知識と経験を持っている人物が行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-143">This step must be done by the database administrator (DBA) or a person who has similar knowledge and experience.</span></span>

<span data-ttu-id="7425f-144">データベースのコピーを作成するには、元のデータベースのバックアップを作成し、新しい名前で復元します。</span><span class="sxs-lookup"><span data-stu-id="7425f-144">To create a database copy, make a backup of the original database, and restore it under a new name.</span></span> <span data-ttu-id="7425f-145">両方のデータベースに十分なスペースがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7425f-145">Make sure that enough space is available for both databases.</span></span> <span data-ttu-id="7425f-146">別のサーバーでコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7425f-146">You can create the copy on a different server.</span></span> <span data-ttu-id="7425f-147">データベースを実行する SQL Server インスタンスのバージョンは重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="7425f-147">The version of the SQL Server instance that runs the database isn't important.</span></span>

<span data-ttu-id="7425f-148">データベースのコピーを作成するコードの例を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7425f-148">Here is an example of the code that creates a database copy.</span></span> <span data-ttu-id="7425f-149">特定のデータベース名を反映するよう、この例を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-149">You must modify this example to reflect your specific database names.</span></span>

```
    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5
```
## <a name="run-the-t-sql-script-to-prepare-the-database"></a><span data-ttu-id="7425f-150">データベースの準備のため T-SQL スクリプトを実行</span><span class="sxs-lookup"><span data-stu-id="7425f-150">Run the T-SQL script to prepare the database</span></span>

<span data-ttu-id="7425f-151">このスクリプトは、ユーザーを削除、AX 2012 RTM モデル ストアに関連するステップを削除、スキーマをクリーンアップ、ビューを削除、および tempDB への参照を削除によってデータベースを準備します。</span><span class="sxs-lookup"><span data-stu-id="7425f-151">This script prepares the database by removing users, removing procedures related to the AX 2012 RTM model store, cleaning up schemas, dropping views, and dropping references to tempDB.</span></span> 

<span data-ttu-id="7425f-152">コピーが作成されたら、次の Transact-SQL (T-SQL) スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-152">After the copy is created, run the following Transact-SQL (T-SQL) script against it.</span></span>

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

## <a name="export-the-copied-database-to-a-bacpac-file"></a><span data-ttu-id="7425f-153">コピーしたデータベースを bacpac ファイルにエクスポートする</span><span class="sxs-lookup"><span data-stu-id="7425f-153">Export the copied database to a bacpac file</span></span>

<span data-ttu-id="7425f-154">SQLPackage.exe ツールを使用して、コピーしたデータベースを bacpac ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7425f-154">Export the copied database to a bacpac file by using the SQLPackage.exe tool.</span></span> <span data-ttu-id="7425f-155">この手順は、DBA または同等の知識を持っているチーム メンバーが行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-155">This step should be done by the DBA or a team member who has equivalent knowledge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7425f-156">この手順を開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="7425f-156">It's very important that you install the latest version of SQL Server Management Studio before you start this step.</span></span> <span data-ttu-id="7425f-157">SQLPackage は以前のバージョンの Management Studio に存在しますが、まず最新バージョンをインストールしない限り、このステップでは正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="7425f-157">Although SQLPackage is present in earlier versions of Management Studio, it won't work correctly for this step unless you first install the latest version.</span></span>


<span data-ttu-id="7425f-158">この手順は重要です。稼動前のダウンタイム中にエクスポートを再度実行する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="7425f-158">This step is important, because the export will have to be done again during the downtime before go-live.</span></span> <span data-ttu-id="7425f-159">いくつかのヒントを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7425f-159">Here are some tips:</span></span>

- <span data-ttu-id="7425f-160">bacpac プロセスでは、I/O および CPU に非常に負荷がかかります。</span><span class="sxs-lookup"><span data-stu-id="7425f-160">The bacpac process is very I/O and CPU intensive.</span></span> <span data-ttu-id="7425f-161">したがって、高性能コンピューターでエクスポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-161">Therefore, run the export on a high-powered machine.</span></span>
- <span data-ttu-id="7425f-162">SQLPackage は、データベースをホストするコンピューターにローカルで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-162">SQLPackage should be run locally on the machine that hosts the database.</span></span> <span data-ttu-id="7425f-163">この処理もネットワーク集中型であるため、データベース コンピューターに接続するローカルのラップトップで SQLPackage を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="7425f-163">Don't run SQLPackage on a local laptop that you connect to the database machine, because this process is also network intensive.</span></span>

<span data-ttu-id="7425f-164">次に、管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-164">Next, open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

<span data-ttu-id="7425f-165">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7425f-165">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="7425f-166">**ssn** (ソース サーバー名) – エクスポートする SQL Server の名前。</span><span class="sxs-lookup"><span data-stu-id="7425f-166">**ssn** (source server name) – The name of the SQL Server to export from.</span></span> <span data-ttu-id="7425f-167">このプロセスでは、このパラメータは常に **localhost** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-167">For our process, this parameter should always be set to **localhost**.</span></span>
- <span data-ttu-id="7425f-168">**sdn** (ソース データベース名) – エクスポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="7425f-168">**sdn** (source database name) – The name of the database to export.</span></span>
- <span data-ttu-id="7425f-169">**tf** (ターゲット ファイル) – エクスポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="7425f-169">**tf** (target file) – The path and name of the file to export to.</span></span> <span data-ttu-id="7425f-170">フォルダーが既に存在するはずですが、ファイルはプロセスによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="7425f-170">The folder should already exist, but the file will be created by the process.</span></span>
- <span data-ttu-id="7425f-171">**/p:CommandTimeout** – クエリあたりのタイムアウト値。</span><span class="sxs-lookup"><span data-stu-id="7425f-171">**/p:CommandTimeout** – The per-query timeout value.</span></span> <span data-ttu-id="7425f-172">このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="7425f-172">This parameter enables larger tables to be exported without hitting a timeout.</span></span>

## <a name="upload-the-bacpac-file-to-azure-storage-or-the-lcs-asset-library"></a><span data-ttu-id="7425f-173">Azure ストレージまたは LCS アセット ライブラリに bacpac ファイルをアップロード</span><span class="sxs-lookup"><span data-stu-id="7425f-173">Upload the bacpac file to Azure storage or the LCS Asset Library</span></span>

<span data-ttu-id="7425f-174">作成した bacpac ファイルは、Azure でホストされたサンドボックス環境の AOS マシンにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-174">The bacpac file you have created will need to be copied to the AOS machine in your Azure hosted sandbox environment.</span></span> <span data-ttu-id="7425f-175">これを引当するためのいくつかの理由があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-175">There are several reasons for this:</span></span>
1. <span data-ttu-id="7425f-176">レベル 2 (またはそれ以上) サンドボックス環境により使用される Azure SQL データベース インスタンスには、環境自体の外からのアクセスを防ぐファイアウォール ルールがあります。</span><span class="sxs-lookup"><span data-stu-id="7425f-176">The Azure SQL Database instance used by your Tier 2 (or higher) sandbox environment has firewall rules preventing access from outside of the environment itself.</span></span>
2. <span data-ttu-id="7425f-177">Bacpac インポートのパフォーマンスは、Azure SQL データベース インスタンスとし同じ Azure データセンター コンピューターからインポートした場合、何倍も向上します。</span><span class="sxs-lookup"><span data-stu-id="7425f-177">Performance of bacpac import is multiple times faster when importing from a machine within the same Azure datacenter as the Azure SQL database instance.</span></span>

<span data-ttu-id="7425f-178">bacpac ファイルを AOS マシンに移動する方法を選択することができます。自分の SFTP または他のセキュアな転送サービスがある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-178">You can choose how you would like to move the bacpac file to the AOS machine - you may have your own SFTP or other secure file transfer service.</span></span> <span data-ttu-id="7425f-179">Azure ストレージを使用することをお勧めします。Azure ストレージを使用するには、ユーザー自身のサブスクリプション (Dynamics サブスクリプション自体に含まれていません)で独自の Azure ストレージ アカウントを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-179">We recommend to use our Azure storage, which would require that you acquire your own Azure storage account on your own Azure subscription (this is not provided within the Dynamics subscription itself).</span></span> <span data-ttu-id="7425f-180">Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは [Azcopy](/azure/storage/storage-use-azcopy) を、GUI 操作からは [Microsoft Azure ストレージ エクスプローラー](https://storageexplorer.com/) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7425f-180">There are free tools to help you to move files between Azure storage, from a command line you can use [Azcopy](/azure/storage/storage-use-azcopy), or for a GUI experience you can use [Microsoft Azure storage explorer](https://storageexplorer.com/).</span></span> <span data-ttu-id="7425f-181">これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="7425f-181">Use one of these tools to first upload the backup from your on-premises environment to Azure storage and then on your download it on your development environment.</span></span>

<span data-ttu-id="7425f-182">もう 1 つの (無料) オプションは、LCS 資産ライブラリを使用することですが、アップロードやダウンロードは Azure ストレージよりも時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-182">Another (free) option is to use the LCS asset library, however, the upload and download will take longer than Azure storage.</span></span> <span data-ttu-id="7425f-183">このオプションを使用するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="7425f-183">To use this option:</span></span>
1. <span data-ttu-id="7425f-184">LCS でプロジェクトにログインし、アセット ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="7425f-184">Log into your project in LCS and go to your Asset library.</span></span>
2. <span data-ttu-id="7425f-185">データベース バックアップ タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7425f-185">Select the Database backup tab.</span></span>
3. <span data-ttu-id="7425f-186">bacpac ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="7425f-186">Upload the bacpac file.</span></span>
<span data-ttu-id="7425f-187">その VM から LCS にログインして LCS アセット ライブラリからダウンロードすることにより、後から bacpac をサンドボックス AOS VM にダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="7425f-187">You can later download the bacpac onto the sandbox AOS VM by logging into LCS on that VM and downloading it from the LCS Asset library.</span></span>

## <a name="import-the-bacpac-file-into-sql-database"></a><span data-ttu-id="7425f-188">bacpac ファイルを SQL Database にインポートする</span><span class="sxs-lookup"><span data-stu-id="7425f-188">Import the bacpac file into SQL Database</span></span>

<span data-ttu-id="7425f-189">この手順では、エクスポートした bacpac ファイルを、サンドボックス環境で使用する SQL データベース インスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="7425f-189">During this step, you will import the exported bacpac file to the SQL Database instance that your sandbox environment uses.</span></span> <span data-ttu-id="7425f-190">まず、サンドボックス AOS コンピューターに Management Studio の最新バージョンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-190">You must first install the latest version of Management Studio on your sandbox AOS machine.</span></span> <span data-ttu-id="7425f-191">その後 SQLPackage.exe ツールを使用してファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="7425f-191">You will then import the file by using the SQLPackage.exe tool.</span></span>


<span data-ttu-id="7425f-192">SQL データベース インスタンスへのアクセスを制限するファイアウォール規則があるため、サンドボックス環境の AOS コンピューターでこれらのタスクを直接実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-192">You will perform these tasks directly on the AOS machine in your sandbox environment, because there are firewall rules that restrict access to the SQL Database instance.</span></span> <span data-ttu-id="7425f-193">ただし、AOS コンピューターを使用すると、アクセス許可を取得できます。</span><span class="sxs-lookup"><span data-stu-id="7425f-193">However, by using the AOS machine, you can gain access.</span></span>

<span data-ttu-id="7425f-194">エクスポートの手順に関しては、インポートを開始する前に、Management Studio の最新バージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="7425f-194">As for the export step, you must have the latest version of Management Studio before you start the import.</span></span> <span data-ttu-id="7425f-195">以前のバージョンを使用している場合、この手順は機能しません。</span><span class="sxs-lookup"><span data-stu-id="7425f-195">This step won't work if you have an older version.</span></span>

<span data-ttu-id="7425f-196">パフォーマンス上の理由から、bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7425f-196">For performance reasons, we recommend that you put the bacpac file on drive D on the AOS machine.</span></span> <span data-ttu-id="7425f-197">Azure 仮想マシン (VM) では、ドライブ D は通常、他の利用可能なディスクよりも高いパフォーマンスを持つ物理ディスクです。</span><span class="sxs-lookup"><span data-stu-id="7425f-197">On Azure virtual machines (VMs), drive D is a physical disk that typically has higher performance than other available disks.</span></span>

<span data-ttu-id="7425f-198">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-198">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

```
    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=<Service objective>
```

<span data-ttu-id="7425f-199">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="7425f-199">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="7425f-200">**tsn** (ターゲット サーバー名) – インポートする SQL Azure サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="7425f-200">**tsn** (target server name) – The name of the SQL Azure server to import to.</span></span> <span data-ttu-id="7425f-201">名前は LCS で確認できます。</span><span class="sxs-lookup"><span data-stu-id="7425f-201">The name can be found in LCS.</span></span> <span data-ttu-id="7425f-202">末尾に **.database.windows.net** を付け加えます。</span><span class="sxs-lookup"><span data-stu-id="7425f-202">Suffix it with **.database.windows.net**.</span></span>
- <span data-ttu-id="7425f-203">**tdn** (ターゲット データベース名) – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="7425f-203">**tdn** (target database name) – The name of the database to import to.</span></span> <span data-ttu-id="7425f-204">データベースが既に存在していない必要があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-204">The database should not already exist.</span></span> <span data-ttu-id="7425f-205">インポート処理が作成されます。</span><span class="sxs-lookup"><span data-stu-id="7425f-205">The import process will create it.</span></span>
- <span data-ttu-id="7425f-206">**sf** (ソース ファイル) – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="7425f-206">**sf** (source file) – The path and name of the file to import from.</span></span>
- <span data-ttu-id="7425f-207">**tp** (ターゲット パスワード) – ターゲット SQL データベース インスタンスの SQL パスワード。</span><span class="sxs-lookup"><span data-stu-id="7425f-207">**tp** (target password) – The SQL password for the target SQL Database instance.</span></span>
- <span data-ttu-id="7425f-208">**tu** (ターゲット ユーザー) – ターゲット SQL データベース インスタンスの SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="7425f-208">**tu** (target user) – The SQL user name for the target SQL Database instance.</span></span> <span data-ttu-id="7425f-209">**sqladmin** を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7425f-209">We recommend that you use **sqladmin**.</span></span> <span data-ttu-id="7425f-210">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="7425f-210">You can retrieve the password for this user from your LCS project.</span></span>
- <span data-ttu-id="7425f-211">**/p:CommandTimeout** – クエリあたりのタイムアウト値。</span><span class="sxs-lookup"><span data-stu-id="7425f-211">**/p:CommandTimeout** – The per-query timeout value.</span></span> <span data-ttu-id="7425f-212">このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="7425f-212">This parameter enables larger tables to be exported without hitting a timeout.</span></span>
- <span data-ttu-id="7425f-213">**/p:DatabaseServiceObjective** - S1、P2、P4 など、データベースのパフォーマンス レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="7425f-213">**/p:DatabaseServiceObjective** – Specifies the performance level of the database such as S1, P2 or P4.</span></span> <span data-ttu-id="7425f-214">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</span><span class="sxs-lookup"><span data-stu-id="7425f-214">To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this envrironment.</span></span> <span data-ttu-id="7425f-215">Management Studio を使用して、既存のデータベースの値を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7425f-215">You can check the value for the existing database by using Management Studio.</span></span> <span data-ttu-id="7425f-216">データベースを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7425f-216">Right-click the database, and then select **Properties**.</span></span>

<span data-ttu-id="7425f-217">コマンドを実行すると、次の警告が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="7425f-217">After you run the commands, you may see the following warning.</span></span> <span data-ttu-id="7425f-218">これは無視してかまいません。</span><span class="sxs-lookup"><span data-stu-id="7425f-218">You can safely ignore it.</span></span>

![サンドボックス エラー](./media/sandbox-2.png)


## <a name="run-a-t-sql-script-to-update-the-database"></a><span data-ttu-id="7425f-220">データベースの更新のため T-SQL スクリプトを実行</span><span class="sxs-lookup"><span data-stu-id="7425f-220">Run a T-SQL script to update the database</span></span>
<span data-ttu-id="7425f-221">インポートされたデータベースに対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-221">Run the following script against the imported database.</span></span> <span data-ttu-id="7425f-222">スクリプトでは次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7425f-222">The script performs the following actions:</span></span>

-   <span data-ttu-id="7425f-223">データベース ユーザーを再作成</span><span class="sxs-lookup"><span data-stu-id="7425f-223">Recreates database users</span></span>
-   <span data-ttu-id="7425f-224">適切な実績パラメーターを設定</span><span class="sxs-lookup"><span data-stu-id="7425f-224">Sets the correct performance parameters</span></span>
-   <span data-ttu-id="7425f-225">SQL Query Store 機能の有効化</span><span class="sxs-lookup"><span data-stu-id="7425f-225">Enables the SQL Query Store feature</span></span>

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

## <a name="run-the-data-upgrade-deployable-package"></a><span data-ttu-id="7425f-226">データ アップグレード展開可能なパッケージを実行</span><span class="sxs-lookup"><span data-stu-id="7425f-226">Run the data upgrade deployable package</span></span>

<span data-ttu-id="7425f-227">最新の Finance and Operations 更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード展開可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共用資産ライブラリから最新のバイナリ更新プログラムをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7425f-227">To get the latest data upgrade deployable package for a target environment that is running the latest Finance and Operations update, download the latest binary updates from Microsoft Dynamics Lifecycle Services (LCS) Shared asset library.</span></span>

1. <span data-ttu-id="7425f-228">[LCS](https://lcs.dynamics.com/)にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7425f-228">Sign in to [LCS](https://lcs.dynamics.com/)</span></span>
2. <span data-ttu-id="7425f-229">**共有資産ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7425f-229">Select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="7425f-230">**共有アセット** ライブラリの**アセット タイプの選択**で、**ソフトウェア配置可能パッケージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7425f-230">In the **Shared asset** library, under **Select asset type**, select **Software deployable package**.</span></span>
4. <span data-ttu-id="7425f-231">配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。</span><span class="sxs-lookup"><span data-stu-id="7425f-231">In the list of deployable package files, find the data upgrade package that corresponds to your upgrade.</span></span> <span data-ttu-id="7425f-232">たとえば、AX 2012 からアップグレードする場合、パッケージ名は AX2012DataUpgrade から始まります。</span><span class="sxs-lookup"><span data-stu-id="7425f-232">For example, if you're upgrading from AX 2012, the package name starts with AX2012DataUpgrade.</span></span> <span data-ttu-id="7425f-233">アップグレードするリリースに対応するパッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="7425f-233">Select the package that corresponds to the release you are upgrading to.</span></span> <span data-ttu-id="7425f-234">例: AX2012DataUpgrade-July2017。</span><span class="sxs-lookup"><span data-stu-id="7425f-234">For example: AX2012DataUpgrade-July2017.</span></span>

<span data-ttu-id="7425f-235">詳細については、[開発、デモ、またはサンドボックス環境でのデータのアップグレード](upgrade-data-to-latest-update.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7425f-235">For more information, see [Upgrade data in development, demo, or sandbox environments](upgrade-data-to-latest-update.md).</span></span> 

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a><span data-ttu-id="7425f-236">データベースのコピーを開発環境でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="7425f-236">Upgrade a copy of the database in a development environment</span></span>

<span data-ttu-id="7425f-237">開発環境で同じデータベースをアップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7425f-237">It is highly recommended to have upgraded the same database in a development environment.</span></span> <span data-ttu-id="7425f-238">開発環境で利用できるデータベースのコピーを使用する場合は、アップグレードされたサンドボックス環境で検出されるバグを調査する方がはるかに簡単です。</span><span class="sxs-lookup"><span data-stu-id="7425f-238">If you have a copy of the database available for development environments, it will be much easier to investigate bugs that are found in the upgraded sandbox environment.</span></span>
