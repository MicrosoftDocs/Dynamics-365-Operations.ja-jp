---
title: オンプレミス環境のインプレース アップグレード プロセス
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e1f81fa4dd2d9c998fd9ae574ad8ba0e954641bb
ms.sourcegitcommit: 8ff2413b6cb504d2b36fce2bb50441b2e690330e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "3082019"
---
# <a name="in-place-upgrade-process-for-on-premises-environments"></a>オンプレミス環境のインプレース アップグレード プロセス

> [!NOTE]
> 実稼働環境のアップグレードを実行する前に、サンドボックス環境のアップグレードを実行してください。

このトピックでは、Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。  

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-8-20-to-81"></a>7.x (プラットフォーム更新プログラム 8 ~ 20) から 8.1 へのオンプレミス アップグレード

> [!NOTE]
> このアップグレード プロセスは完了に時間がかかり、データ アップグレード中はずっと Finance and Operations が使用できなくなります。

7.x から 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。

各パスの概要は下に記載されています。

-   **VHD 内からのアップグレード** - このパスは、仮想ハード ディスク (VHD) に、データベースをコピーし、その中のアップグレードを実行します。 全体的に、この方法はよりシンプルです。

-   **データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。 アップグレード プロセスは、VHD 内からも実行されます。

> [!NOTE]
> VHD では、アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。

### <a name="prerequisites"></a>必要条件

1.  Lifecycle Services (LCS) では、共有資産ライブラリ (画面の右側にある) に移動します。

2.  **資産タイプの選択**で、**ダウンロード可能な VHD** を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。 すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。

3.  ダウンロードしたファイルは、自己展開する zip ファイルです。 少なくとも 86 GBの空き領域に VHD を展開します。

4.  Hyper-V を使用して、仮想マシン (VM) を起動し、VHD を接続します。 (マシンはジェネレーション 1 である必要があります。)

5.  VM に接続します。 資格情報を[仮想マシン (VM) をローカルで実行](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally)から見つけることができます。

6.  拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。 アップグレード前に、環境を準備する必要がある場合は、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。

### <a name="upgrading-from-within-vhd"></a>VHD 内からのアップグレード

1.  オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または各ノードで Service Fabric Host Service を停止し、無効にします。

2.  オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。 詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。

3.  VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。

4.  任意の場所にファイルを貼り付け、展開します。 たとえば、c:\\D365FFOUpgrade\\ です。

5.  管理者としてコマンド プロンプトを開き、手順 4 で展開していないフォルダーへディレクトリを変更します。

6.  Onebox VM に作成したバックアップを復元します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。

7.  オプション: 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```
    > [!NOTE] 
    > (たとえば、AXDB などの) 適切な値に <DB-Name> を置き換えます。 値をさらに編集する場合は、付録 A を参照します。

    スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。

8.  手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。

    a.  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    b.  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    c.  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります。 
    
    `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`
    
    これを解決するには、次のコマンドのステップを再実行します。 
    
    `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`

9.  アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。 ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。

10. 実稼働環境用から (たとえば、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。

11. オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

12. LCS でプロジェクトを開き、**環境**セクションで展開を削除します。 アプリケーションが環境の Service Fabric Explorer から表示されなくなります。 このプロセスは、持っているノードの数に応じて、時間がかかることがあります。 新しい環境を配置する前に、Service Fabric Explorer を確認し、すべての申請が削除されていることを確認します。 実際のプロセスが完了する前に、LCS では環境が削除されていることを示す場合があることに注意してください。

13. カスタマイズする場合、次の事項を行います。

    a.  LCS では、共有資産ライブラリに移動します。

    b.  **資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。

    c.  SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。
     
    d.  データベースを構成する必要があります。 [Finance and Operations データベースのコンフィギュレーション](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database) の手順に従います。

    e.  LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。 配置する場合、指定するデータベースは手順 13 c (通常は AXDB) で作成したものにする必要があります。

    f.  独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。 それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。

    g.  オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。

    h.  名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。

    i.  オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

14. カスタマイズを持っていない場合は、次の事項を実行します。

    a.  (省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。 次の手順で、アップグレードされたデータベースの名前を入力することを確認します。

    b.  LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。

15. (省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a>データベースを指す VHD でアップグレードする

1.  オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。

2.  オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。 詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。

3.  先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。

4.  接続されたら、C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。

5.  任意の場所にファイルを貼り付け、展開します。 たとえば、C:\\D365FFOUpgrade\\ です。

6.  管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。

7.  管理者として新しい PowerShell を開き、次のように実行します。
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > \<\*\> を必要な値に置き換えます。

    > [!NOTE]
    > - SQL Server 認証のみが、このアップグレードで正式にサポートされます。 詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。
    >
    > - SQL Server 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。 詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。
    >
    > - 使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。 これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。
    >
    > - Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。 そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。

8.  手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。

    a.  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    b.  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    c.  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`

    これを解決するには、次のコマンドのステップを再実行します: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`

9.  ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。

10. オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

11. LCS でプロジェクトを開き、**環境**セクションで展開を削除します。 アプリケーションが環境の Service Fabric Explorer から表示されなくなります。 このプロセスは、持っているノードの数に応じて、時間がかかることがあります。

12. カスタマイズする場合、次の事項を行います。

    a.  LCS では、共有資産ライブラリに移動します。

    b.  **資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。

    c.  SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。

    d.  データベースを構成する必要があります。 [Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。

    e.  LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。 配置する場合、指定する必要があるデータベースは手順 12 c (通常は AXDB) で作成したものにする必要があります。

    f.  独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。 それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。

    g.  オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。

    h.  名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。

    i.  オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

13. カスタマイズを持っていない場合は、次の事項を実行します。

    a.  (省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。 次の手順で、アップグレードされたデータベースの名前を入力することを確認します。

    b.  新しい環境を設定し、バージョン 8.1 で配置します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。

14. (省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-21-or-later-to-81"></a>7.x (プラットフォーム更新プログラム 21 以降) から 8.1 へのオンプレミス アップグレード

> [!NOTE]
> このアップグレード プロセスは完了に時間がかかり、プロセス中はずっと Finance and Operations が使用できなくなります。

オンプレミス 7.x からオンプレミス 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。

各パスの概要は下に記載されています。

-   **VHD 内からのアップグレード** - このパスは、VHD にデータベースをコピーし、その中のアップグレードを実行します。 全体的に、この方法はよりシンプルです。

-   **データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。 アップグレード プロセスは、VHD 内からも実行されます。
    
> [!NOTE]
> VHD では、データ アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。


### <a name="prerequisites"></a>必要条件

1.  LCS では、共有資産ライブラリ (画面の右側にある) に移動します。

2.  **資産タイプの選択**で、ダウンロード可能な VHD を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。 すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。

3.  ダウンロードしたファイルは、自己展開する zip ファイルです。 少なくとも 86 GBの空き領域に VHD を展開します。

4.  Hyper-V を使用して、VM を起動し、VHD を接続します。 (マシンはジェネレーション 1 である必要があります。)

5.  VM に接続します。 資格情報についてはこちらをご覧ください。https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally

6.  続行する前に、VHD のプラットフォームのバージョンを、環境にあるものと同じ状態になるようにアップグレードする必要があります。 基本的には、環境内のバージョン番号と正確に一致するように VHD 内のプラットフォームのバージョン数を計算する必要があります。 これを行うには、LCS で環境の履歴を確認し、資産ライブラリからどのパッケージが適用されているかを確認できます。 VHD が既にプラットフォーム更新 プログラム 20 (7.0.5030.35333) に含まれているため、環境に手動でインストールした一部のパッケージが既に含まれていますが、環境に適用した最新のバイナリ更新プログラムが含まれていない可能性があります。

7.  パッケージまたは適用する必要があるパッケージを検索した後に、LCS から VHD にそれをダウンロードします。

8.  各パッケージについては、次の操作を行います。

    a.  c:\\D365FFOUpgrade\\ などのパッケージを展開します。

    b.  管理者としてコマンド プロンプトを開き、展開していないフォルダーへディレクトリを変更します。

    c.  実行

       1. `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

       2. `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

       3. `AxUpdateInstaller.exe execute -runbookid=upgrade`

9.  アプリケーションの拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。 アップグレード前に、どんな方法でも環境を準備する必要がある場合は、ISV または VAR に確認します。

### <a name="upgrading-from-within-vhd"></a>VHD 内からのアップグレード

1.  オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。

2.  オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。 詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。

3.  VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。

4.  任意の場所にファイルを貼り付け、展開します。 例 c:\\D365FFOUpgrade\\

5.  管理者としてコマンド プロンプトを開き、手順 4 で展開したフォルダーへディレクトリを変更します。

6.  Onebox VM に作成したバックアップを復元します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。

7.  (オプション) 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```

    > [!NOTE] 
    > (通常、AXDB などの) 適切な値に \<DB-Name\> を置き換えます。 値をさらに編集する場合は、付録 A を参照します。

    スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。

8.  手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。

    a.  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    b.  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    c.  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`

    これを解決するには、次のコマンドのステップを再実行します: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`

9.  アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。 ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。

10. 実稼働環境用から (通常、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。

11. オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

12. LCS でプロジェクトを開き、**環境**セクションで展開を削除します。 アプリケーションが環境の Service Fabric Explorer から表示されなくなります。 このプロセスは、持っているノードの数に応じて、時間がかかることがあります。

13. LCS では、共有資産ライブラリに移動します。

14. **資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。

15. SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。

16. データベースを構成する必要があります。 [Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。

17. LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。 配置する場合、指定する必要があるデータベースは手順 15 (通常は AXDB) で作成したものにする必要があります。

18. 独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。 それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。

19. オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。

20. 名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。

21. オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

22. (省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a>データベースを指す VHD でアップグレードする

1.  オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。

2.  オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。 詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。

3.  先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。

4.  VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。

5.  C:\\D365FFOUpgrade\\ など、任意の展開場所にファイルを貼り付けます。

6.  管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。

7.  管理者として新しい PowerShell を開き、次のように実行します。

    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > \<\*\> を必要な値に置き換えます。

    > [!NOTE]
    > - SQL Server 認証のみが、このアップグレードで正式にサポートされます。 詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。
    >
    > - SQL サーバー 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。 詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。 
    >
    > - 使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。 これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。
    >
    > - Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。 そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。

8.  手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。

    a.  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    b.  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    c.  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`

    この問題を解決するには、次のコマンドのステップを再実行します: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`

9.  ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。

10. オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

11. LCS でプロジェクトを開き、**環境**セクションで展開を削除します。 アプリケーションが環境の Service Fabric Explorer から表示されなくなります。 このプロセスは、持っているノードの数に応じて、時間がかかることがあります。

12. LCS では、共有資産ライブラリに移動します。

13. **資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。

14. SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。 詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。

15. データベースを構成する必要があります。 [Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。

16. LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。 詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。 配置する場合、指定する必要があるデータベースは手順 14 (通常は AXDB) で作成したものにする必要があります。

17. 独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。 それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。

18. オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。

19. 名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。

20. オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。

21. (省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="appendix-a"></a>付録 A

### <a name="configure-on-premises-upgradeps1-usage"></a>Configure-On-Premises-Upgrade.ps1 の使用状況

> [!Important]
> このスクリプトは、Onebox VHD 環境からの実行のみを目的としています。
>
> スクリプトは、少なくとも DatabaseName パラメーターを渡すことを必要としています。 渡さないと、スクリプトは自動的に要求します。

DatabaseServer または DatabaseUser のような追加のパラメーターを渡す場合は、これを行うことができますが、スクリプトはすべての追加のパラメータを要求するようになります。 これは、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するため起こりますが、これらのパラメーターは、正しく接続を確立する必要があります。

スクリプトに渡することができるパラメーターは次の通りです。

-   **-DatabaseName** - アップグレードするデータベースの名前です。

-   **-DatabaseServer** - Finance and Operations (オンプレミス) データベースが含まれているデータベース サーバーです。

-   **-DatabaseUser** - SQL 認証のユーザー名です。

-   **-DatabasePassword** - SQL 認証のパスワードです。

コンフィギュレーションが渡された後に、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。 スクリプトが接続されない場合は、Microsoft SQL Server Management Studio を使用するか、またはその他のツールを使用して、接続をデバッグすることをお勧めします。

**Configure-On-Premises-Upgrade.ps1**

```powershell
<#
.Synopsis
   Configures a Onebox deployment to upgrade an OnPrem 7.x database to OnPrem 8.x 

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

-   データベース名が間違っているまたはユーザーがそのデータベースにアクセスできない場合は、例外を呼び出します。\"0\" 引数で\"開きます\"。\"ログインによって要求されたデータベース \"AxDB1\" を開くことができません。 ログインに失敗しました。 ユーザー、\'axdbadmin\'.\" のログインが失敗しました。

-   接続が確立できませんでした。 Ip/fqdn とポートを確認します。例外を呼び出します。\"0\" 引数で\"開きます\"。\"SQL Server への接続を確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。 サーバーが見つからない、またはアクセスできませんでした。 インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。 (プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした)\"

-   ログイン資格情報が正確ではありません。 例外 の呼び出し: \"0\" 引数で\"開きます\"。\"ユーザー \'axdbadmin\' のログインが失敗しました。\"
