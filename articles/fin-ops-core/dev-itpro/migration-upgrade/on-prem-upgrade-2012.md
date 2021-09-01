---
title: Dynamics 365 Finance + Operations (オンプレミス) への AX 2012 のデータ アップグレード プロセス
description: このトピックでは、Microsoft Dynamics AX 2012 データベースを Dynamics 365 Finance  + Operations (オンプレミス) 10.0.X にアップグレードするプロセスについて説明します。
author: faix
ms.date: 12/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fecb4bc2d714cf122eb9c29a4bea394e55f8c338a21bbacb3a5bfde7833cc4b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731517"
---
# <a name="data-upgrade-process-for-ax-2012-to-dynamics-365-finance--operations-on-premises"></a>Dynamics 365 Finance + Operations (オンプレミス) への AX 2012 のデータ アップグレード プロセス

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 データベースを Dynamics 365 Finance  + Operations (オンプレミス) 10.0.X にアップグレードするプロセスについて説明します。 現在、Dynamics AX 2012 R2 または Dynamics AX 2012 R3 のいずれかからのアップグレードのみ、サポートされています。 

> [!IMPORTANT]
> このトピックでは、データ アップグレードを行う手順についてのみ説明します。 コード アップグレードを実行する方法の詳細については、クラウド バージョンで使用可能なアップグレード ガイドを参照してください。 コード アップグレード ツールは、Microsoft Dynamics Lifecycle Services (LCS) を介してのみ使用可能です。

## <a name="ax-2012-upgrade-to-dynamics-365-finance--operations-on-premises"></a>AX 2012 を Dynamics 365 Finance + Operations (オンプレミス) にアップグレードする

現在、サポートされているアップグレード方法は 2 つあります。

- **VHD 内からのアップグレード** – この方法では、データベースを仮想ハード ディスク (VHD) にコピーし、VHD 内からアップグレードを実行します。 全体的に、この方法は簡単です。
- **データベースを指す VHD でアップグレード** – この方法は、VHD アップグレード プロセスをデータベースにポイントします。 アップグレード プロセスは、VHD 内から実行されます。

> [!NOTE]
> VHDがアップグレード プロセスを実行するのに、外部のネットワーク アクセス権は必要ありません。

### <a name="prerequisites"></a>必要条件

1. [プレビュー サブスクリプションへのサインアップ](upgrade-overview-2012.md#sign-up-for-a-preview-subscription)。
1. 各 AX 2012 リリースについては、Finance + Operations アプリケーションの最新リリースにアップグレードする前に、利用可能な最新の累積更新プログラムに更新します。
1. アップグレード前のチェックリストをインストールします。 詳細については、[インストール](prepare-data-upgrade.md#installation) を参照してください。
1. データ アップグレードの準備手順を実行します。 「ユーザー マッピングの設定」の手順はスキップできます。 この手順は、クラウドでホストされているアップグレードのみ関連しています。
1. データベースのバックアップを作成します (MicrosoftDynamicsAX)。 詳細については、「[フル データベース バックアップの作成](/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2016)」を参照してください。
1. LCS で、ページの右側にあるタイルを選択して、共有アセット ライブラリに移動します。 **資産タイプの選択** の下の **ダウンロード可能な VHD** を選択し、オンプレミス環境でアップグレードするバージョンに最も適合する VHD パッケージ全体をダウンロードします。 画像は大量のディスク容量を必要とします。 したがって、十分な空き領域のあるドライブでパッケージをダウンロードし、展開する必要があります。 
1. ダウンロードしたファイルは、自己展開する zip ファイルです。 十分な空き容量が確保されている場所に VHD を展開してください。
1. Hyper-V を使用して、仮想マシン (VM) を開始し、VHD を接続します。 (VM はジェネレーション 1 である必要があります。)
1. VM に接続します。 資格情報の詳細については、[ローカルで仮想マシン (VM) を実行する](../dev-tools/access-instances.md#running-the-virtual-machine-locally) を参照してください。
1. オンプレミスで予定されている 10.0.x のターゲット バージョンとダウンロードした VHD イメージによっては、 共有アセット ライブラリから必要なアプリケーション更新プログラムとプラットフォーム更新プログラムをダウンロードして適用することが必要となる場合があります。 **アセット タイプの選択** で、**ソフトウェア配置可能パッケージ** を選択します。 詳細な情報については、[コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md) を参照してください。

    > [!IMPORTANT]
    > いずれの場合でも、最新の品質更新プログラムが VHD に適用されていることを確認し、データ アップグレードを実行するための最新の修正プログラムが含まれていることを確認してください。 

1. 拡張機能またはカスタマイズがある場合、今 VHD にインストールしてください。 それ以外の場合、アップグレード プロセスは、カスタマイズに関連するデータをすべて削除します。 アップグレードの前に、環境を準備する必要がある場合、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。

### <a name="upgrade-from-inside-the-vhd"></a>VHD 内からアップグレードする

1. Onebox VM に作成したバックアップを復元します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016)」を参照してください。
1. オプション: 復元したデータベースの名前が **axdb** でない場合、管理者として Windows PowerShell を開き、次のスクリプトを実行します。

    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```

    > [!NOTE] 
    > **\<DB-name\>** をデータベースの名前 (**AXDB** など) で置き換えます。 多くの値を編集する場合、このトピックの [付録](#appendix) を参照してください。

    スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを検証します。

1. LCS では、共有アセット ライブラリに移動します。 **アセット タイプの選択** で **ソフトウェア配置可能パッケージ** を選択し、**AX2012DataUpgrade-10-0-8** を選択して、**MajorVersionDataUpgrade.zip** をダウンロードします。
1. ファイルをコピーして目的の場所に貼り付け (**c:\\D365FFOUpgrade\\** など)、展開します。
1. 管理者としてコマンド プロンプト ウィンドウを開き、展開したフォルダーへディレクトリを変更して、次のコマンドを実行します。

    1. `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`
    2. `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`
    3. `AxUpdateInstaller.exe execute -runbookid=upgrade`

1. アップグレード プロセスが正常に完了した後、新たにアップグレードしたデータベースをバックアップします。 ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。
1. データベースをオンプレミス環境の SQL Server に復元し、AX 2012 データベースの名前とは異なる名前 (**AXDBupgraded** など) を付けます。 復元したデータベースはコンフィギュレーションする必要があります。 [Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。
1. 新しい Dynamics 365 Finance + Operations (オンプレミス) 環境を配置します。

    - カスタマイズがある場合、次の手順に従います。

        1. LCS では、共有アセット ライブラリに移動します。
        1. **資産タイプの選択** の下で、**モデル** を選択し、**Dynamics 365 Finance + Operations オンプレミスのバージョン 10.0.x デモ データ** をダウンロードします。 オンプレミスのベースラインとして展開する 10.0.x 環境に最も近いバージョンを選択します。
        1. このファイルから新しいデータベースを作成するのには、SQL Server に対して復元バックアップ オプションを使用します。 (通常、このデータベースには **AXDB** という名前が付けられます。) 詳細については、[SSMS を使用したデータベース バックアップの復元](/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017) を参照してください。
        1. デモ データベースはコンフィギュレーションする必要があります。 [Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。
        1. LCS で新しい環境を設定し、バージョン 10.0.x で配置します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。 環境を配置する場合、事前に作成したデータベースの名前 (通常は **AXDB**) を指定する必要があります。
        1. 新たに作成した 10.0.x 環境と ISV および VAR モジュールにカスタマイズを適用します。 それ以外の場合、この環境が最初にデータベースと同期される時、カスタマイズ関連または拡張機能関連のデータが削除されます。
        1. オンプレミスの Application Object Server (AOS)、ビジネス インテリジェンス (BI)、および Management Reporter (MR) サーバーをシャットダウンするか、または **無効化 (再起動)** を選択して、Azure Service Fabric ポータルからサービスを停止します。
        1. 名前を変更するか、配置で使用したデモ データベース (通常は **AXDB**) を削除して、新しいデータベース (通常は **AXDBupgraded**) の名前を、デモ データベースが使用していた名前 (通常は **AXDB**) に変更します。
        1. 名前を変更したデータベースはコンフィギュレーションする必要があります。 [Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。
        1. オンプレミス AOS、BI、および MR サーバーを開始するか、または **有効化** を選択して Service Fabric ポータルからサービスを開始します。

            > [!NOTE]
            > AOS ノードの開始時にデータベースの同期プロセスがトリガーされますが、プロセスが完了するまで環境は使用できません。

    - カスタマイズがない場合、次の手順に従います。

        1. オプション: 既存のデータベース (通常は **AXDBold**) の名前を変更し、新しいデータベース (通常は **AXDB**) の名前を変更します。 次の手順で、アップグレードされたデータベース名の入力を確認します。
        2. LCS にて、新たな環境を設定し、バージョン 10.0.x (再展開) を展開します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。

### <a name="upgrade-where-the-vhd-points-to-your-database"></a>VHD がデータベースをポイントする場所でアップグレードする

1. オンプレミス環境 (通常は **AXDB**) から、データベースをバックアップします。 詳細については、「[フル データベース バックアップの作成 (SQL Server)](/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2016)」を参照してください。
1. 先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (**AXDBtoupgrade** など) を付けます。 詳細については、「[SSMS を使用したデータベース バックアップの復元](/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016)」を参照してください。
1. 管理者として Windows PowerShell を開き、次のスクリプトを実行します。

    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > - **\<DB-name\>**、**\<SqlServerName\>**、**\<User\>**、および **\<Password\>** を必要な値に置換します。
    > - SQL Server 認証のみが、このアップグレードで正式にサポートされます。 詳細については、「[データベース ユーザーの作成](/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2016)」を参照してください。
    > - SQL Server 証明書に署名した証明機関の証明書を、OneBox VHD の信頼された証明機関ストアに追加する必要があります。 詳細については、「[信頼されたルート証明書をインストールする](/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。
    > - 使用するデータベースのユーザーに、**sysadmin** サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくとも **すべての特権** があるかを確認します。 また、ユーザーに tempDB にアクセスするためのアクセス許可があることを確認します。 これらの条件を満たしていない場合、アップグレード プロセスのステップ 6 は失敗します。
    > - 証明機関の証明書を OneBox VHD にインストールする場合、そこに表示されるデータベースへ接続するには完全修飾ドメイン名 (FQDN) または IP アドレスを使用してください。 サーバーを指していないため、ドメイン名を使用してデータベースにアクセスできない場合は、ホスト ファイルを編集して FQDN が解決する必要がある FQDN と IP アドレスを追加します。

1. LCS では、共有アセット ライブラリに移動します。 **アセット タイプの選択** で **ソフトウェア配置可能パッケージ** を選択し、**AX2012DataUpgrade-10-0-8** を選択して、**MajorVersionDataUpgrade.zip** をダウンロードします。
1. ファイルをコピーして目的の場所に貼り付け (**c:\\D365FFOUpgrade\\** など)、展開します。
1. 管理者としてコマンド プロンプト ウィンドウを開き、展開したフォルダーへディレクトリを変更して、次のコマンドを実行します。

    1. `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`
    2. `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`
    3. `AxUpdateInstaller.exe execute -runbookid=upgrade`

1. ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。
1. このトピックの後半にある [VHD データベースのリセット (オプション)](#resetting-the-vhd-database-optional) セクションで記述されている値を使用して **Configure-OnpremUpgrade.ps1** スクリプトを実行します。
1. [Finance + Operations データベースのコンフィギュレーション](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database) の手順に従って、Finance + Operations に対してアップグレードしたデータベースをコンフィギュレーションします。
1. 新しい Dynamics 365 Finance + Operations (オンプレミス) 環境を配置します。

    - カスタマイズがある場合、次の手順に従います。

        1. LCS では、共有アセット ライブラリに移動します。
        1. **資産タイプの選択** の下で、**モデル** を選択し、**Dynamics 365 Finance + Operations オンプレミスのバージョン 10.0.x デモ データ** をダウンロードします。 オンプレミスのベースラインとして展開する 10.0.x 環境に最も近いバージョンを選択します。
        1. SQL Server に対して復元バックアップ オプションを使用して、このファイルから新しいデータベース (通常は **AXDB**) を作成します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016)」を参照してください。
        1. デモ データベースはコンフィギュレーションする必要があります。 [Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。
        1. LCS にて、新たな環境を設定し、バージョン 10.0.x (再展開) を展開します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。 環境を配置する場合、事前にコンフィギュレーションしたデータベースの名前 (通常は **AXDB**) を指定する必要があります。
        1. 新たに作成した 10.0.x 環境と ISV および VAR モジュールにカスタマイズを適用します。 それ以外の場合、この環境が最初にデータベースと同期される時、カスタマイズ関連または拡張機能関連のデータが削除されます。
        1. オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。
        1. 名前を変更するか、配置で使用したデモ データベース (通常は **AXDB**) を削除して、新しいデータベース (通常は **AXDBupgraded**) の名前を、デモ データベースが使用していた名前 (通常は **AXDB**) に変更します。
        1. オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

            > [!NOTE]
            > AOS ノードの開始時にデータベースの同期プロセスがトリガーされますが、プロセスが完了するまで環境は使用できません。

    - カスタマイズがない場合、次の手順に従います。

        1. オプション: 既存のデータベース (通常は **AXDBold**) の名前を変更し、新しいデータベース (通常は **AXDB**) の名前を変更します。 次の手順で、アップグレードされたデータベース名の入力を確認します。
        2. 新しい環境を設定し、バージョン 10.0.x で配置します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。

### <a name="configuring-existing-users"></a>既存のユーザーのコンフィギュレーション

以前の手順のいずれかに従った場合、LCS で指定した管理者ユーザーを使用してサインインできます。 ただし、他のユーザーは、新しいシステム用にコンフィギュレーションされるまで、サインインできません。 USERINFO テーブルに対して **Select** ステートメントを実行し、管理者ユーザーの **NETWORKDOMAIN** フィールドの値 (`https://adfs.contoso.com/adfs` または `http://adfs.contoso.com/adfs/services/trust` など) をメモしておき ます。 サインインできる必要のあるすべての対話型ユーザーについて、**NETWORKDOMAIN** フィールドに管理者ユーザーと同じ値を設定します。 **NETWORKALIAS** フィールドも変更する必要があります。 Finance + Operations において、このフィールドにはユーザーの電子メールアドレス (`testuser@contoso.com` など) が設定され ます。

### <a name="resetting-the-vhd-database-optional"></a>VHD データベースのリセット (オプション)

**Configure-On-Premises-Upgrade.ps1** スクリプトを使用した場合、次のコマンドを実行してデータベースを既定のコンフィギュレーションにリセットします。

```powershell
.\Configure-OnPremUpgrade.ps1 -DatabaseName 'AxDB' -DatabaseServer 'localhost' -DatabaseUser 'axdbadmin' -DatabasePassword 'AOSWebSite@123'
```

## <a name="appendix"></a>付録

### <a name="using-the-configure-on-premises-upgradeps1-script"></a>Configure-On-Premises-Upgrade.ps1 スクリプトを使用する

> [!IMPORTANT]
> このスクリプトは、OneBox VHD 環境からの実行のみを目的としています。
>
> スクリプトは、少なくとも **DatabaseName** パラメーターを渡すことを必要としています。 このパラメーターを渡さないと、スクリプトは自動的に要求します。

必要に応じて、**DatabaseServer** または **DatabaseUser** などの追加のパラメーターを渡すことができます。 ただし、この場合は、スクリプトはすべての追加のパラメーターを要求します。 この現象は、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するために発生します。 したがって、これらのパラメータは接続を正しく確立するのに必要です。

次のパラメーターをスクリプトに渡することができます。

- **-DatabaseName** – アップグレードするデータベースの名前。
- **-DatabaseServer** – Finance + Operations データベースが含まれているデータベース サーバー。
- **-DatabaseUser** – SQL Server 認証のためのユーザー名。
- **-DatabasePassword** – SQL Server 認証のためのパスワードです。

コンフィギュレーションが渡された後、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。 スクリプトがデータベースに接続できない場合は、SQL Server Management Studio または別のツールを使用して、接続をデバッグすることをお勧めします。

**Configure-On-Premises-Upgrade.ps1**

```powershell
<#
.Synopsis
    Configures a OneBox deployment to upgrade an OnPrem 7.x database to OnPrem 10.0.x 

.DESCRIPTION
    This must be executed before the upgrade process is carried out.

.EXAMPLE
    .\Configure-OnPremUpgrade.ps1 -DatabaseName 'AxDB'

    .\Configure-OnPremUpgrade.ps1 -DatabaseName 'AxDB' -DatabaseServer '127.0.0.1' -DatabaseUser 'axdbadmin' -DatabasePassword 'secretPass'
#>
[CmdletBinding()]
param
(
    # Database server containing Microsoft Dynamics 365 for Operations, on-premises database.
    [AllowNull()]
    [string] $DatabaseServer,

    # Database name that you want to upgrade.
    [Parameter(Mandatory = $true)]
    [string] $DatabaseName,

    # Username for SQL Authentication.
    [AllowNull()]
    [string] $DatabaseUser,

    # Password for SQL Authentication.
    [AllowNull()]
    [string] $DatabasePassword
)

$webroot = "C:\AOSService\webroot"

$commandParameter = " -decrypt `"$webroot\web.config`""

$command = Resolve-Path "$webroot\bin\Microsoft.Dynamics.AX.Framework.ConfigEncryptor.exe"

Start-Process $command $commandParameter -PassThru -Wait

if([string]::IsNullOrEmpty($DatabaseUser) -and [string]::IsNullOrEmpty($DatabasePassword) -and [string]::IsNullOrEmpty($DatabaseServer)) { 

    [xml]$web = Get-Content $webroot\web.config

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.Database']").value = [string]$DatabaseName

}
else { 

    if([string]::IsNullOrEmpty($DatabaseServer)){

        $DatabaseServer = if($value = Read-Host 'What is the IP or FQDN of the Database server? [127.0.0.1]') {$value} else {'127.0.0.1'}

    }

    if([string]::IsNullOrEmpty($DatabaseUser)){

        $DatabaseUser = if($value = Read-Host 'What is the SQL Authentication username? [axdbadmin]') {$value} else {'axdbadmin'}

    }

    if([string]::IsNullOrEmpty($DatabasePassword)){

        $dbPassEn = if($value = Read-Host 'What is the SQL Authentication password?' -AsSecureString) {$value} else {''}

        $BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($dbPassEn) 

        $DatabasePassword = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)

    } 

    [xml]$web = Get-Content $webroot\web.config

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.DbServer']").value = [string]$DatabaseServer

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.Database']").value = [string]$DatabaseName

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlUser']").value = [string]$DatabaseUser

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlPwd']").value = [string]$DatabasePassword

}
#Save Configuration to webroot config
$web.Save("$webroot\web.config")

#Reloading the configuration to run test
[xml]$web = Get-Content $webroot\web.config

$TestDbServer = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.DbServer']").value

$TestDbName = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.Database']").value

$TestDbUser = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlUser']").value

$TestDbPass = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlPwd']").value

#Setting up connection test.

$dbConn = New-Object System.Data.SqlClient.SqlConnection

$dbConn.ConnectionString = "Data Source=$TestDbServer;User ID=$TestDbUser;Password=`"$TestDbPass`";Database=$TestDbName"

try{

    $dbConn.Open()

    $result = $true

}

catch{

    $result = $_.Exception.Message

}
Finally{

    $dbConn.Close()

}

$commandParameter = " -encrypt `"$webroot\web.config`""

Start-Process $command $commandParameter -PassThru -Wait

if($result -ne $true){

    Write-Host "`nThe connection to the Database Server failed:" -ForegroundColor Red
    Write-Host $result -ForegroundColor Red

}
else{

    Write-Host "`nThe connection to the Database Server was successful!" -ForegroundColor Green

}
```

### <a name="troubleshooting"></a>トラブルシューティング

- "0" 引数を使用した "Open" の呼び出しで例外が発生しました: 「ログインによって要求されたデータベース「AxDB1」を開くことはできません。 ログインに失敗しました。 ユーザー 'axdbadmin' のログインが失敗しました。」データベース名が間違っている、またはユーザーにデータベースへのアクセスがありません。 
- "0" 引数を使用した "Open" の呼び出しで例外が発生しました: SQL Server への接続の確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。 サーバーが見つからない、またはアクセスできませんでした。 インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。 (プロバイダー: 名前付きパイプ プロバイダー、エラー: 40 - SQL Server への接続を開けませんでした)。 スクリプトは、指定された SQL Server との接続を確立できませんでした。 使用した IP/FQDN およびポートを確認します。  
- "0" 引数を使用した "Open" の呼び出しで例外が発生しました: 「ユーザー 'axdbadmin' のログインが失敗しました。」指定されたログイン資格情報が正確ではありません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]