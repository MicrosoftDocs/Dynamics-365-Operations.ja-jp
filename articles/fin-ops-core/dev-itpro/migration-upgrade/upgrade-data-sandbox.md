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
# <a name="upgrade-from-ax-2012---data-upgrade-in-sandbox-environments"></a><span data-ttu-id="07c77-103">AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード</span><span class="sxs-lookup"><span data-stu-id="07c77-103">Upgrade from AX 2012 - Data upgrade in sandbox environments</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

> [!NOTE]
> <span data-ttu-id="07c77-104">このトピックは段階的に廃止され、dacpac ファイル形式に基づく新しいプロセスが採用されます。</span><span class="sxs-lookup"><span data-stu-id="07c77-104">This topic is being phased out in favor of a new process that is based on the dacpac file format.</span></span> <span data-ttu-id="07c77-105">新しいプロセスの詳細については、「[AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境からデータをアップグレードするための DACPAC プロセス](upgrade-data-sandbox-dacpac.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-105">For information about the new process, see [Upgrade from AX 2012 - Dacpac process to upgrade data in Sandbox Tiers 2-5 environments](upgrade-data-sandbox-dacpac.md).</span></span>

<span data-ttu-id="07c77-106">このタスクの出力は、サンドボックス環境で使用できるデータベースのアップグレードです。</span><span class="sxs-lookup"><span data-stu-id="07c77-106">The output of this task is an upgraded database that you can use in a sandbox environment.</span></span> <span data-ttu-id="07c77-107">このトピックでは、*サンドボックス* という用語は、SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2/3)、またはより高度な環境を示します。</span><span class="sxs-lookup"><span data-stu-id="07c77-107">In this topic, we use the term *sandbox* to refer to a Standard or Premier Acceptance Testing (Tier 2/3) or higher environment connected to a SQL Azure database.</span></span> <span data-ttu-id="07c77-108">この環境では、ビジネス ユーザーと機能チームのメンバーがアプリケーション機能を検証できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-108">On this environment business users and functional team members can validate application functionality.</span></span> <span data-ttu-id="07c77-109">この機能には、カスタマイズ内容や Microsoft Dynamics AX 2012 から継承されたデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07c77-109">This functionality includes customizations and the data that was brought forward from Microsoft Dynamics AX 2012.</span></span>

<span data-ttu-id="07c77-110">この方法は、データを正常にアップグレードするのに必要な全体的な時間の短縮に役立つため、共有サンドボックス環境で実行する前に開発環境でデータ アップグレード プロセスを実行することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-110">We strongly recommend that you run the data upgrade process in a development environment before you run it in a shared sandbox environment, because this approach will help reduce the overall time that is required for a successful data upgrade.</span></span> <span data-ttu-id="07c77-111">詳細については[AX 2012からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト](prepare-data-upgrade.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-111">For more information, see [Upgrade from AX 2012 - Pre-upgrade checklist for data upgrade](prepare-data-upgrade.md).</span></span>

> [!NOTE]
> <span data-ttu-id="07c77-112">このプロセスを開始する前に、SQLPackage の最新バージョンをインストールすることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="07c77-112">It's very important that you install the latest version of SQLPackage before you start this process.</span></span> <span data-ttu-id="07c77-113">これを行うには、[SQLPackage のダウンロードとインストール](/sql/tools/sqlpackage-download) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-113">To do this, go to [Download and Install SQLPackage](/sql/tools/sqlpackage-download).</span></span> <span data-ttu-id="07c77-114">.NET Core バージョンの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-114">We recommend that you use the .NET Core version.</span></span> <span data-ttu-id="07c77-115">これは C:\temp に保存および抽出することができます。</span><span class="sxs-lookup"><span data-stu-id="07c77-115">This can be saved and extracted to C:\temp.</span></span>

## <a name="overview-of-the-sandbox-data-upgrade-process"></a><span data-ttu-id="07c77-116">サンドボックス データ アップグレード プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="07c77-116">Overview of the sandbox data upgrade process</span></span>
<span data-ttu-id="07c77-117">サンドボックス環境でのデータのアップグレードを開始する前に、[AX 2012 からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト](prepare-data-upgrade.md)で説明しているように、開発環境で既にデータがアップグレードされています。</span><span class="sxs-lookup"><span data-stu-id="07c77-117">Before you start to upgrade data in a sandbox environment, you will have already upgraded data in a development environment, as explained in [Upgrade from AX 2012 - Pre-upgrade checklist for data upgrade](prepare-data-upgrade.md).</span></span> <span data-ttu-id="07c77-118">2 つのプロセスはよく似ています。</span><span class="sxs-lookup"><span data-stu-id="07c77-118">The two processes are very similar.</span></span> <span data-ttu-id="07c77-119">主な違いは、サンドボックス環境では Microsoft Azure SQL データベースをデータ保管に使用し、開発環境では Microsoft SQL Server を使用する点です。</span><span class="sxs-lookup"><span data-stu-id="07c77-119">The main difference is that a sandbox environment uses Microsoft Azure SQL Database for data storage, whereas a development environment uses Microsoft SQL Server.</span></span> <span data-ttu-id="07c77-120">このデータベース レイヤーの技術的な違いにより、AX 2012 データベース インスタンスからのバックアップを SQL データベースに復元できないため、サンドボックス環境でデータのアップグレード手順を少し変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-120">This technical difference in the database layer requires that you  modify the data upgrade procedure slightly in a sandbox environment, because a backup from the AX 2012 database instance can't just be restored to SQL Database.</span></span>

![サンドボックス データのアップグレード プロセス](./media/data-upgrade-sandbox.png)

<span data-ttu-id="07c77-122">アップグレード プロセスの高レベルの手順を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="07c77-122">Here are the high-level steps in the upgrade process.</span></span>

1. <span data-ttu-id="07c77-123">AX 2012 AOS インスタンスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="07c77-123">Turn off the AX 2012 AOS instances.</span></span>
2. <span data-ttu-id="07c77-124">AX 2012 データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="07c77-124">Create a copy of the AX 2012 database.</span></span> <span data-ttu-id="07c77-125">エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-125">We strongly recommend that you use a copy, because you must delete some objects in the copy that will be exported.</span></span>
3. <span data-ttu-id="07c77-126">SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="07c77-126">Export the copied database to a bacpac file by using a free SQL Server tool that is named SQLPackage.exe.</span></span> <span data-ttu-id="07c77-127">このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。</span><span class="sxs-lookup"><span data-stu-id="07c77-127">This tool provides a special type of database backup that can be imported into SQL Database.</span></span>
4. <span data-ttu-id="07c77-128">オプションで、クラウドでホストされている VM からインポートを実行している場合は、bacpac ファイルを Azure ストレージにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-128">Optional, if you are running import from a cloud-hosted VM, you should upload the bacpac file to Azure storage.</span></span> 
5. <span data-ttu-id="07c77-129">SQLPackage.exe を使用して bacpac ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="07c77-129">Import the bacpac file by using SQLPackage.exe.</span></span> <span data-ttu-id="07c77-130">ローカル サーバーまたはクラウドでホストされている VM から実行できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-130">This can be run from a local server or from a cloud-hosted VM.</span></span> <span data-ttu-id="07c77-131">ローカル サーバーを使用する場合は、Dynamics 365 データベースへの JIT アクセスを要求し、必要なファイアウォール ルールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-131">If you’re using a local server, you will need to request JIT access to the Dynamics 365 database and set the required firewall rules.</span></span> <span data-ttu-id="07c77-132">クラウドでホストされている VM を使用している場合は、bacpac ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="07c77-132">If you’re using a cloud-hosted VM, download the bacpac file.</span></span> <span data-ttu-id="07c77-133">SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-133">You must then run a script against the imported database to reset the SQL database users.</span></span>

6. <span data-ttu-id="07c77-134">インポートされたデータベースに対して適切なデータ アップグレード パッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="07c77-134">Run the appropriate data upgrade package against the imported database.</span></span>

## <a name="turn-off-the-ax-2012-aos-instances"></a><span data-ttu-id="07c77-135">AX 2012 AOS インスタンスをオフにします</span><span class="sxs-lookup"><span data-stu-id="07c77-135">Turn off the AX 2012 AOS instances</span></span>

<span data-ttu-id="07c77-136">このタスクには、AX 2012 のシステム管理者とサーバー管理者が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07c77-136">This task involves the AX 2012 system administrator and the server administrators.</span></span>

<span data-ttu-id="07c77-137">AOS インスタンスをオフにする前に、実行しているすべてのバッチ ジョブを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-137">Before you turn off AOS instances, you must stop all batch jobs that are running.</span></span> <span data-ttu-id="07c77-138">既に稼働し始めている実行時間の長いバッチ ジョブでは、システムが停止しないようにします。</span><span class="sxs-lookup"><span data-stu-id="07c77-138">A long-running batch job that has already started to run will prevent the system from stopping.</span></span> <span data-ttu-id="07c77-139">必要な場合は AOS インスタンスを停止できるように、事前に計画してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-139">Plan ahead, so that you can stop your AOS instances when needed.</span></span> <span data-ttu-id="07c77-140">AX 2012 をオフにする前にバッチが完了するよう、バッチをスケジュールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-140">You might have to schedule batches so that they're completed some time before you turn off AX 2012.</span></span>

<span data-ttu-id="07c77-141">AX 2012 環境と統合されている他のシステムをお持ちかもしれません。</span><span class="sxs-lookup"><span data-stu-id="07c77-141">You might have other systems that are integrated with the AX 2012 environment.</span></span> <span data-ttu-id="07c77-142">AX 2012 をオフにするための計画には、これらのシステムも考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-142">You must also factor these systems into your plan to turn off AX 2012.</span></span> <span data-ttu-id="07c77-143">たとえば、AX 2012 自体をオフにする前に、統合システムをしばらくオフにして、残りのインフライト トランザクションを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-143">For example, you might have to turn off the integrated systems some time before you turn off AX 2012 itself, so that any remaining in-flight transactions can be completed.</span></span> <span data-ttu-id="07c77-144">統合システムの要件は、企業間で広く異なります。</span><span class="sxs-lookup"><span data-stu-id="07c77-144">The requirements for integrated systems vary widely from business to business.</span></span> <span data-ttu-id="07c77-145">したがって、専門家チームはこのシナリオを個別に計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-145">Therefore, your team of experts must plan for this scenario independently.</span></span>

## <a name="create-a-copy-of-the-ax-2012-database"></a><span data-ttu-id="07c77-146">AX 2012 データベースのコピーの作成</span><span class="sxs-lookup"><span data-stu-id="07c77-146">Create a copy of the AX 2012 database</span></span>

<span data-ttu-id="07c77-147">データベースから一部のオブジェクトを削除する必要があるため、アップグレードを実行している AX 2012 データベースのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-147">You must create a copy of the AX 2012 database that you're upgrading, because you must delete some objects from the database.</span></span> <span data-ttu-id="07c77-148">これらのオブジェクトには、Microsoft Windows 認証ユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="07c77-148">These objects include any Microsoft Windows authentication users.</span></span> <span data-ttu-id="07c77-149">これらの変更により、変更されたデータベースは AX 2012 で使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="07c77-149">These changes make the modified database unusable for AX 2012.</span></span> <span data-ttu-id="07c77-150">この手順では、データベースのコピーを作成してこれらのオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="07c77-150">During this step, you will create a copy of the database and delete these objects.</span></span>

<span data-ttu-id="07c77-151">この手順は、データベース管理者 (DBA) または同様の知識と経験を持っている人物が行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-151">This step must be done by the database administrator (DBA) or a person who has similar knowledge and experience.</span></span>

<span data-ttu-id="07c77-152">データベースのコピーを作成するには、元のデータベースのバックアップを作成し、新しい名前で復元します。</span><span class="sxs-lookup"><span data-stu-id="07c77-152">To create a database copy, make a backup of the original database, and restore it under a new name.</span></span> <span data-ttu-id="07c77-153">両方のデータベースに十分なスペースがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="07c77-153">Make sure that enough space is available for both databases.</span></span> <span data-ttu-id="07c77-154">別のサーバーでコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-154">You can create the copy on a different server.</span></span> <span data-ttu-id="07c77-155">データベースを実行する SQL Server インスタンスのバージョンは重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="07c77-155">The version of the SQL Server instance that runs the database isn't important.</span></span>

<span data-ttu-id="07c77-156">このアクションを実行するには、ソースデータベースを右クリックし、**タスク** \> **バックアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07c77-156">To perform this action, right-click the source database, and then select **Tasks** \> **Backup**.</span></span> <span data-ttu-id="07c77-157">フル コピー バックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="07c77-157">Create a full-copy backup.</span></span> <span data-ttu-id="07c77-158">既存のデータベースのバックアップが上書きされないようにするために、ファイルを別の名前でバックアップ ディレクトリに保存することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-158">To avoid overwriting your existing database backups, you might want to save the file under a different name in the backup directory.</span></span>

## <a name="run-the-t-sql-script-to-prepare-the-database"></a><span data-ttu-id="07c77-159">データベースの準備のため T-SQL スクリプトを実行</span><span class="sxs-lookup"><span data-stu-id="07c77-159">Run the T-SQL script to prepare the database</span></span>

<span data-ttu-id="07c77-160">このスクリプトは、ユーザーを削除、AX 2012 RTM モデル ストアに関連するステップを削除、スキーマをクリーンアップ、ビューを削除、および tempDB への参照を削除によってデータベースを準備します。</span><span class="sxs-lookup"><span data-stu-id="07c77-160">This script prepares the database by removing users, removing procedures related to the AX 2012 RTM model store, cleaning up schemas, dropping views, and dropping references to tempDB.</span></span> 

<span data-ttu-id="07c77-161">コピーが作成されたら、次の Transact-SQL (T-SQL) スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="07c77-161">After the copy is created, run the following Transact-SQL (T-SQL) script against it.</span></span>

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

## <a name="export-the-copied-database-to-a-bacpac-file"></a><span data-ttu-id="07c77-162">コピーしたデータベースを bacpac ファイルにエクスポートする</span><span class="sxs-lookup"><span data-stu-id="07c77-162">Export the copied database to a bacpac file</span></span>

> [!NOTE]
> <span data-ttu-id="07c77-163">このトピックは段階的に廃止され、dacpac ファイル形式に基づく新しいプロセスが採用されます。</span><span class="sxs-lookup"><span data-stu-id="07c77-163">This topic is being phased out in favor of a new process that is based on the dacpac file format.</span></span> <span data-ttu-id="07c77-164">新しいプロセスの詳細については、「[AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境からデータをアップグレードするための DACPAC プロセス](upgrade-data-sandbox-dacpac.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-164">For information about the new process, see [Upgrade from AX 2012 - Dacpac process to upgrade data in Sandbox Tiers 2-5 environments](upgrade-data-sandbox-dacpac.md).</span></span>

<span data-ttu-id="07c77-165">SQLPackage.exe ツールを使用して、コピーしたデータベースを bacpac ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="07c77-165">Export the copied database to a bacpac file by using the SQLPackage.exe tool.</span></span> <span data-ttu-id="07c77-166">この手順は、DBA または同等の知識を持っているチーム メンバーが行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-166">This step should be done by the DBA or a team member who has equivalent knowledge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07c77-167">この手順を開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="07c77-167">It's very important that you install the latest version of SQL Server Management Studio before you start this step.</span></span> <span data-ttu-id="07c77-168">SQLPackage は以前のバージョンの Management Studio に存在しますが、まず最新バージョンをインストールしない限り、このステップでは正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="07c77-168">Although SQLPackage is present in earlier versions of Management Studio, it won't work correctly for this step unless you first install the latest version.</span></span>


<span data-ttu-id="07c77-169">この手順は重要です。稼動前のダウンタイム中にエクスポートを再度実行する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="07c77-169">This step is important, because the export will have to be done again during the downtime before go-live.</span></span> <span data-ttu-id="07c77-170">いくつかのヒントを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="07c77-170">Here are some tips:</span></span>

- <span data-ttu-id="07c77-171">bacpac プロセスでは、I/O および CPU に非常に負荷がかかります。</span><span class="sxs-lookup"><span data-stu-id="07c77-171">The bacpac process is very I/O and CPU intensive.</span></span> <span data-ttu-id="07c77-172">したがって、高性能コンピューターでエクスポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="07c77-172">Therefore, run the export on a high-powered machine.</span></span>
- <span data-ttu-id="07c77-173">SQLPackage は、データベースをホストするコンピューターにローカルで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-173">SQLPackage should be run locally on the machine that hosts the database.</span></span> <span data-ttu-id="07c77-174">この処理もネットワーク集中型であるため、データベース コンピューターに接続するローカルのラップトップで SQLPackage を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="07c77-174">Don't run SQLPackage on a local laptop that you connect to the database machine, because this process is also network intensive.</span></span>

<span data-ttu-id="07c77-175">次に、管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="07c77-175">Next, open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

```Console
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

<span data-ttu-id="07c77-176">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="07c77-176">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="07c77-177">**ssn** (ソース サーバー名) – エクスポートする SQL Server の名前。</span><span class="sxs-lookup"><span data-stu-id="07c77-177">**ssn** (source server name) – The name of the SQL Server to export from.</span></span> <span data-ttu-id="07c77-178">このプロセスでは、パラメータは常に **localhost** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-178">For this process, the parameter should always be set to **localhost**.</span></span>
- <span data-ttu-id="07c77-179">**sdn** (ソース データベース名) – エクスポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="07c77-179">**sdn** (source database name) – The name of the database to export.</span></span>
- <span data-ttu-id="07c77-180">**tf** (ターゲット ファイル) – エクスポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="07c77-180">**tf** (target file) – The path and name of the file to export to.</span></span> <span data-ttu-id="07c77-181">フォルダーが既に存在するはずですが、ファイルはプロセスによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="07c77-181">The folder should already exist, but the file will be created by the process.</span></span>
- <span data-ttu-id="07c77-182">**/p:CommandTimeout** – クエリあたりのタイムアウト値。</span><span class="sxs-lookup"><span data-stu-id="07c77-182">**/p:CommandTimeout** – The per-query timeout value.</span></span> <span data-ttu-id="07c77-183">このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="07c77-183">This parameter enables larger tables to be exported without a timeout.</span></span>

## <a name="upload-the-bacpac-file-to-azure-storage-or-the-lcs-asset-library"></a><span data-ttu-id="07c77-184">Azure ストレージまたは LCS アセット ライブラリに bacpac ファイルをアップロード</span><span class="sxs-lookup"><span data-stu-id="07c77-184">Upload the bacpac file to Azure storage or the LCS Asset Library</span></span>

<span data-ttu-id="07c77-185">作成した bacpac ファイルは、Azure でホストされたサンドボックス環境の AOS マシンにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-185">The bacpac file you have created will need to be copied to the AOS machine in your Azure hosted sandbox environment.</span></span> <span data-ttu-id="07c77-186">これを引当するためのいくつかの理由があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-186">There are several reasons for this:</span></span>
1. <span data-ttu-id="07c77-187">レベル 2 (またはそれ以上) サンドボックス環境により使用される Azure SQL データベース インスタンスには、環境自体の外からのアクセスを防ぐファイアウォール ルールがあります。</span><span class="sxs-lookup"><span data-stu-id="07c77-187">The Azure SQL Database instance used by your Tier 2 (or higher) sandbox environment has firewall rules preventing access from outside of the environment itself.</span></span>
2. <span data-ttu-id="07c77-188">Bacpac インポートのパフォーマンスは、Azure SQL データベース インスタンスとし同じ Azure データセンター コンピューターからインポートした場合、何倍も向上します。</span><span class="sxs-lookup"><span data-stu-id="07c77-188">Performance of bacpac import is multiple times faster when importing from a machine within the same Azure datacenter as the Azure SQL database instance.</span></span>

<span data-ttu-id="07c77-189">bacpac ファイルを AOS マシンに移動する方法を選択することができます。自分の SFTP または他のセキュアな転送サービスがある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-189">You can choose how you would like to move the bacpac file to the AOS machine - you may have your own SFTP or other secure file transfer service.</span></span> <span data-ttu-id="07c77-190">Azure ストレージを使用することをお勧めします。Azure ストレージを使用するには、ユーザー自身のサブスクリプション (Dynamics サブスクリプション自体に含まれていません)で独自の Azure ストレージ アカウントを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-190">We recommend to use our Azure storage, which would require that you acquire your own Azure storage account on your own Azure subscription (this is not provided within the Dynamics subscription itself).</span></span> <span data-ttu-id="07c77-191">Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは [Azcopy](/azure/storage/storage-use-azcopy) を、GUI 操作からは [Microsoft Azure Storage Explorer](https://storageexplorer.com/) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-191">There are free tools to help you to move files between Azure storage, from a command line you can use [Azcopy](/azure/storage/storage-use-azcopy), or for a GUI experience you can use [Microsoft Azure storage explorer](https://storageexplorer.com/).</span></span> <span data-ttu-id="07c77-192">これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="07c77-192">Use one of these tools to first upload the backup from your on-premises environment to Azure storage and then on your download it on your development environment.</span></span>

<span data-ttu-id="07c77-193">Microsoft Dynamics Lifecycle Services (LCS) でアセット ライブラリを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="07c77-193">Another option is to use the Asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="07c77-194">ただし、アップロードとダウンロードには、Azure ストレージよりも長い時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="07c77-194">However, the upload and download will take longer than Azure storage.</span></span> <span data-ttu-id="07c77-195">このオプションを使用するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="07c77-195">To use this option:</span></span>
1. <span data-ttu-id="07c77-196">LCS でプロジェクトにサインインし、アセット ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="07c77-196">Sign in to your project in LCS and go to your Asset library.</span></span>
2. <span data-ttu-id="07c77-197">データベース バックアップ タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="07c77-197">Select the Database backup tab.</span></span>
3. <span data-ttu-id="07c77-198">bacpac ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="07c77-198">Upload the bacpac file.</span></span>
<span data-ttu-id="07c77-199">サンドボックス AOS サーバーへの RDP アクセスが削除されたため、サンドボックス環境と同じリージョンで実行されているクラウド ホスト環境を使用してファイルをインポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-199">Since the removal of RDP access to Sandbox AOS servers, we recommend that you use a cloud-hosted environment running in the same region as the sandbox environment to import the file.</span></span> <span data-ttu-id="07c77-200">クラウドでホストされている VM に bacpac ファイルをダウンロードするには、そのコンピューターの LCS にサインインし、LCS アセット ライブラリからダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="07c77-200">You can download the bacpac onto the cloud-hosted VM by signing in to LCS on that machine and downloading it from the LCS Asset library.</span></span>

## <a name="import-the-bacpac-file-into-sql-database"></a><span data-ttu-id="07c77-201">bacpac ファイルを SQL Database にインポートする</span><span class="sxs-lookup"><span data-stu-id="07c77-201">Import the bacpac file into SQL Database</span></span>

> [!NOTE]
> <span data-ttu-id="07c77-202">このトピックは段階的に廃止され、dacpac ファイル形式に基づく新しいプロセスが採用されます。</span><span class="sxs-lookup"><span data-stu-id="07c77-202">This topic is being phased out in favor of a new process that is based on the dacpac file format.</span></span> <span data-ttu-id="07c77-203">新しいプロセスの詳細については、「[AX 2012 からのアップグレード - レベル 2 からレベル 5 のサンドボックス環境からデータをアップグレードするための DACPAC プロセス](upgrade-data-sandbox-dacpac.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-203">For information about the new process, see [Upgrade from AX 2012 - Dacpac process to upgrade data in Sandbox Tiers 2-5 environments](upgrade-data-sandbox-dacpac.md).</span></span>

<span data-ttu-id="07c77-204">この手順では、エクスポートした bacpac ファイルを、サンドボックス環境で使用する SQL Server データベース インスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="07c77-204">During this step, you will import the exported bacpac file into the SQL Server database instance that your sandbox environment uses.</span></span> <span data-ttu-id="07c77-205">上記のように、サンドボックス AOS サーバーへの RDP アクセスが削除されたため、サンドボックス環境と同じリージョンで実行されているクラウド ホスト環境を使用してファイルをインポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-205">As stated above, since the removal of RDP access to Sandbox AOS servers, we recommend that you use a cloud-hosted environment running in the same region as the sandbox environment to import the file.</span></span> <span data-ttu-id="07c77-206">データベースへの JIT アクセスを要求し、ローカル サーバーから実行することができます。</span><span class="sxs-lookup"><span data-stu-id="07c77-206">You can request JIT access to the database and run from a local server.</span></span> <span data-ttu-id="07c77-207">この操作を行うには、[ジャストインタイム データベース アクセスの有効化](../database/database-just-in-time-JIT-access.md)のプロセスに従って、IP アドレスをデータベースの許可リストにします。</span><span class="sxs-lookup"><span data-stu-id="07c77-207">To do that, follow the process for [Enable just-in-time database access](../database/database-just-in-time-JIT-access.md) to allow-list your IP address to the database.</span></span>

<span data-ttu-id="07c77-208">最初に、クラウドでホストされている VM またはローカル サーバーに Management Studio の最新バージョンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-208">You must first install the latest version of Management Studio on your cloud-hosted VM or local server.</span></span> <span data-ttu-id="07c77-209">その後 SQLPackage.exe ツールを使用してファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="07c77-209">You will then import the file by using the SQLPackage.exe tool.</span></span>

<span data-ttu-id="07c77-210">クラウド ホスト環境を使用している場合は、パフォーマンス上の理由から、AOS マシンのドライブ D に bacpac ファイルを配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-210">If you are using a cloud-hosted environment, for performance reasons, we recommend that you put the bacpac file on drive D on the AOS machine.</span></span> <span data-ttu-id="07c77-211">Azure 仮想マシン (VM) では、ドライブ D は通常、他の利用可能なディスクよりも高いパフォーマンスを持つ物理ディスクです。</span><span class="sxs-lookup"><span data-stu-id="07c77-211">On Azure virtual machines (VMs), drive D is a physical disk that typically has higher performance than other available disks.</span></span>

<span data-ttu-id="07c77-212">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="07c77-212">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

```Console
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tdn:<New database name> /tu:sqladmin /tp:<password from LCS> /mp:64 /p:CommandTimeout=1200 /p:DatabaseEdition=<Edition> /p:DatabaseServiceObjective=<Service objective> /p:DatabaseMaximumSize=<Maximum size>
```

<span data-ttu-id="07c77-213">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="07c77-213">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="07c77-214">**sf** (ソース ファイル) – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="07c77-214">**sf** (source file) – The path and name of the file to import from.</span></span>
- <span data-ttu-id="07c77-215">**tsn** (ターゲット サーバー名) – インポートする SQL Azure サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="07c77-215">**tsn** (target server name) – The name of the SQL Azure server to import to.</span></span> <span data-ttu-id="07c77-216">名前は LCS で確認できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-216">The name can be found in LCS.</span></span> <span data-ttu-id="07c77-217">末尾に **.database.windows.net** を付け加えます。</span><span class="sxs-lookup"><span data-stu-id="07c77-217">Suffix it with **.database.windows.net**.</span></span>
- <span data-ttu-id="07c77-218">**tdn** (ターゲット データベース名) – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="07c77-218">**tdn** (target database name) – The name of the database to import to.</span></span> <span data-ttu-id="07c77-219">データベースが既に存在していない必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-219">The database should not already exist.</span></span> <span data-ttu-id="07c77-220">インポート処理が作成されます。</span><span class="sxs-lookup"><span data-stu-id="07c77-220">The import process will create it.</span></span>
- <span data-ttu-id="07c77-221">**tu** (ターゲット ユーザー) – ターゲット SQL データベース インスタンスの SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="07c77-221">**tu** (target user) – The SQL user name for the target SQL Database instance.</span></span> <span data-ttu-id="07c77-222">**sqladmin** を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-222">We recommend that you use **sqladmin**.</span></span> <span data-ttu-id="07c77-223">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-223">You can retrieve the password for this user from your LCS project.</span></span>
- <span data-ttu-id="07c77-224">**tp** (ターゲット パスワード) – ターゲット SQL データベース インスタンスの SQL パスワード。</span><span class="sxs-lookup"><span data-stu-id="07c77-224">**tp** (target password) – The SQL password for the target SQL database instance.</span></span>
- <span data-ttu-id="07c77-225">**mp** (最大並列処理) - データベースに対して実行される同時操作の並列度を指定します。</span><span class="sxs-lookup"><span data-stu-id="07c77-225">**mp** (max parallelism) - Specifies the degree of parallelism for concurrent operations running against a database.</span></span> <span data-ttu-id="07c77-226">既定値は 8 です。</span><span class="sxs-lookup"><span data-stu-id="07c77-226">The default value is 8.</span></span> <span data-ttu-id="07c77-227">値を 64 にすると、ほとんどの場合に最高のパフォーマンスが得られます。</span><span class="sxs-lookup"><span data-stu-id="07c77-227">A value of 64 provides the best performance in most scenarios.</span></span>
- <span data-ttu-id="07c77-228">**/p:CommandTimeout** – クエリあたりのタイムアウト値。</span><span class="sxs-lookup"><span data-stu-id="07c77-228">**/p:CommandTimeout** – The per-query timeout value.</span></span> <span data-ttu-id="07c77-229">このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="07c77-229">This parameter enables larger tables to be exported without a timeout.</span></span>
- <span data-ttu-id="07c77-230">**/p:DatabaseEdition** – Basic、Standard、Premium、GeneralPurpose、BusinessCritical、Hyperscale などのデータベースのエディションを指定します。</span><span class="sxs-lookup"><span data-stu-id="07c77-230">**/p:DatabaseEdition** – Specifies the edition of the database such as Basic, Standard, Premium, GeneralPurpose, BusinessCritical, or Hyperscale.</span></span> <span data-ttu-id="07c77-231">パフォーマンス要件を満たし、サービス契約を遵守するには、この環境で現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="07c77-231">To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</span></span> <span data-ttu-id="07c77-232">Management Studio を使用して、既存のデータベースの値を確認できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-232">You can check the value for the existing database by using Management Studio.</span></span> <span data-ttu-id="07c77-233">データベースを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07c77-233">Right-click the database, and then select **Properties**.</span></span>
- <span data-ttu-id="07c77-234">**/p:DatabaseServiceObjective** - S1、P2、P4 または GP_Gen5_8 など、データベースのパフォーマンス レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="07c77-234">**/p:DatabaseServiceObjective** – Specifies the performance level of the database such as S1, P2, P4, or GP_Gen5_8.</span></span> <span data-ttu-id="07c77-235">パフォーマンス要件を満たし、サービス契約を遵守するには、この環境で現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="07c77-235">To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</span></span> <span data-ttu-id="07c77-236">Management Studio を使用して、既存のデータベースの値を確認できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-236">You can check the value for the existing database by using Management Studio.</span></span> <span data-ttu-id="07c77-237">データベースを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07c77-237">Right-click the database, and then select **Properties**.</span></span>
- <span data-ttu-id="07c77-238">**/p:DatabaseMaximumSize** – Azure SQL データベースの最大サイズを GB 単位で定義します。</span><span class="sxs-lookup"><span data-stu-id="07c77-238">**/p:DatabaseMaximumSize** – Defines the maximum size in GB of an Azure SQL database.</span></span> <span data-ttu-id="07c77-239">大きなデータベースをインポートできるようにするには、このパラメータを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-239">You may need to use this parameter to allow a large database to be imported.</span></span>

<span data-ttu-id="07c77-240">コマンドを実行すると、次の警告を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-240">After you run the commands, you may receive the following warning.</span></span> <span data-ttu-id="07c77-241">これは無視してかまいません。</span><span class="sxs-lookup"><span data-stu-id="07c77-241">You can safely ignore it.</span></span>

![サンドボックス エラー](./media/sandbox-2.png)

<span data-ttu-id="07c77-243">無効な値に関するエラー メッセージを受け取る場合は、パラメータを再確認してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-243">If you receive an error message about a non-valid value, double-check your parameters.</span></span> <span data-ttu-id="07c77-244">問題がない場合は、新しいバージョンの SqlPackage を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-244">If they are okay, you may need to use a newer version of SqlPackage.</span></span> <span data-ttu-id="07c77-245">[Windows .NET Core](/sql/tools/sqlpackage-download) バージョンをインストールすることなく使用できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-245">You can use the [Windows .NET Core](/sql/tools/sqlpackage-download) version without the need to install.</span></span> <span data-ttu-id="07c77-246">これは、たとえば、C:\Temp\Sqlpackage-dotnetcore に抽出できる .zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="07c77-246">It is a .zip file that can be extracted to C:\Temp\Sqlpackage-dotnetcore, for example.</span></span> <span data-ttu-id="07c77-247">これで、データベースをインポートするときに、C:\Program Files (x86) の下で Sqlpackage.exe を使用する代わりに、C:\Temp\Sqlpackage-dotnetcore で Sqlpackage.exe を使用できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-247">Now when you import the database, instead of using the Sqlpackage.exe under C:\Program Files (x86) you can use the Sqlpackage.exe in C:\Temp\Sqlpackage-dotnetcore.</span></span>


## <a name="run-a-t-sql-script-to-update-the-database"></a><span data-ttu-id="07c77-248">データベースの更新のため T-SQL スクリプトを実行</span><span class="sxs-lookup"><span data-stu-id="07c77-248">Run a T-SQL script to update the database</span></span>
<span data-ttu-id="07c77-249">インポートされたデータベースに対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="07c77-249">Run the following script against the imported database.</span></span> <span data-ttu-id="07c77-250">スクリプトでは次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="07c77-250">The script performs the following actions:</span></span>

-   <span data-ttu-id="07c77-251">データベース ユーザーを再作成</span><span class="sxs-lookup"><span data-stu-id="07c77-251">Recreates database users</span></span>
-   <span data-ttu-id="07c77-252">適切な実績パラメーターを設定</span><span class="sxs-lookup"><span data-stu-id="07c77-252">Sets the correct performance parameters</span></span>
-   <span data-ttu-id="07c77-253">SQL Query Store 機能の有効化</span><span class="sxs-lookup"><span data-stu-id="07c77-253">Enables the SQL Query Store feature</span></span>

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

## <a name="run-the-data-upgrade-deployable-package"></a><span data-ttu-id="07c77-254">データ アップグレード展開可能なパッケージを実行</span><span class="sxs-lookup"><span data-stu-id="07c77-254">Run the data upgrade deployable package</span></span>

<span data-ttu-id="07c77-255">レベル 2 のサンドボックス環境では、レベル 1 の DevTest 環境と同様に、データ アップグレード パッケージを LCS から直接実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="07c77-255">For Tier-2 sandbox environments, you can now run the data upgrade package directly from LCS, just as you can do for Tier-1 DevTest environments.</span></span> <span data-ttu-id="07c77-256">パッケージを適用するには、LCS の環境に移動し、**メンテナンス** \> **更新プログラムの適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07c77-256">To apply the package, go to your environment in LCS, and select **Maintain** \> **Apply updates**.</span></span> <span data-ttu-id="07c77-257">一覧の一番下までスクロールし、共用資産ライブラリからデータ アップグレード パッケージが読み込まれるまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="07c77-257">Scroll to the bottom of the list, and wait for the data upgrade packages to be loaded from the Shared asset library.</span></span> <span data-ttu-id="07c77-258">パッケージが読み込まれるまでにしばらく時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-258">It might take some time for the packages to be loaded.</span></span> <span data-ttu-id="07c77-259">リストにデータ アップグレード パッケージが表示されない場合は、LCS のプロジェクト設定に移動し、レガシ システムが **AX2012 アップグレード** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-259">If no data upgrade packages appear in the list, go to your project settings in LCS, and make sure that your legacy system is set to **AX2012 Upgrade**.</span></span> <span data-ttu-id="07c77-260">その後、パッケージを適用できます。</span><span class="sxs-lookup"><span data-stu-id="07c77-260">You can then apply the packages.</span></span>

<span data-ttu-id="07c77-261">選択するパッケージの名前は、使用しているバージョンと一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c77-261">The name of the package that you select should match your version.</span></span> <span data-ttu-id="07c77-262">たとえば、バージョン 10.0.14 にアップグレードするには、**AX2012DataUpgrade-10-0-14** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07c77-262">For example, to upgrade to version 10.0.14, select **AX2012DataUpgrade-10-0-14**.</span></span>

<span data-ttu-id="07c77-263">詳細については、 [開発、デモ、サンドボックス環境でのデータの更新](upgrade-data-to-latest-update.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07c77-263">For more information, see [Upgrade data in development or demo environments](upgrade-data-to-latest-update.md).</span></span> 

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a><span data-ttu-id="07c77-264">データベースのコピーを開発環境でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="07c77-264">Upgrade a copy of the database in a development environment</span></span>

<span data-ttu-id="07c77-265">開発環境で同じデータベースをアップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07c77-265">It is highly recommended to have upgraded the same database in a development environment.</span></span> <span data-ttu-id="07c77-266">開発環境で利用できるデータベースのコピーを使用する場合は、アップグレードされたサンドボックス環境で検出されるバグを調査する方がはるかに簡単です。</span><span class="sxs-lookup"><span data-stu-id="07c77-266">If you have a copy of the database available for development environments, it will be much easier to investigate bugs that are found in the upgraded sandbox environment.</span></span>
