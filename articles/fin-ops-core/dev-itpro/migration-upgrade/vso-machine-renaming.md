---
title: ローカル開発 (VHD) 環境の名前変更
description: このトピックでは、複数のコンピューター間で Microsoft Azure DevOps プロジェクトにアクセスし、1 つのバージョンのサービスの更新プログラムを正常にインストールできるように、ローカル開発 (VHD) 環境の名前を変更する方法について説明します。
author: MargoC
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 25911
ms.assetid: 4f5ff29b-9ae5-4ba2-8b6e-1e5d94e004b3
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e059b8d5684bca4805e53ea8bb6ea1e3d2beea4d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979712"
---
# <a name="rename-a-local-development-vhd-environment"></a>ローカル開発 (VHD) 環境の名前変更

[!include [banner](../includes/banner.md)]

ローカル開発 (VHD) 環境では、次のシナリオで名前を変更する必要があります。

* **複数のコンピューター間で 1 つの Microsoft Azure DevOps プロジェクトにアクセスする:** Azure DevOps がバージョン管理のために必要です。 開発トポロジでは、複数の仮想マシン (VM) が同じコンピューター名である場合、同じ Azure DevOps プロジェクトにアクセスできません。 Azure DevOps はマシン名を ID として使用します。 Microsoft Dynamics Lifecycle Services (LCS) からダウンロードされたローカル VM で開発する場合は、問題が発生する可能性があります。
* **1 つのバージョンのサービスの更新プログラムをインストールする:** 8.1.x などの 1 つのバージョンのサービス更新プログラムを、runbook を使用して VHD 環境にインストールする必要があります。 Runbook が正常に完了するようにするため、VHD 環境の名前を変更する必要があります。 このトピックに記載されているその他の手順を実行する必要もあります。

## <a name="rename-the-machine"></a>コンピューターの名前を変更する
開発を開始するか Azure DevOps に接続する前にマシンの名前を変更してリブートします。 新しい名前が Azure DevOps プロジェクトで使用されるすべてのコンピューター間で一意であることを確認します。

## <a name="update-the-server-name-in-sql-server"></a>SQL Server でサーバー名を更新する
次のコマンドを実行して、Microsoft SQL Server 2016 でサーバー名を更新します。 

```sql
sp_dropserver [old_name];
GO
sp_addserver [new_name], local;
GO
```

これらのコマンドでは、必ず **old\_name** をサーバーの古い名前に、**new\_name** を新しい名前に置き換えてください。 既定では、古い名前は **MININT-F36S5EH** ですが、**select @@servername** を実行して古い名前を取得できます。 また、コマンドの実行が完了した後、必ず SQL Server サービスを再起動してください。

## <a name="update-sql-server-reporting-services"></a>SQL Server Reporting Services の更新
Reporting Services 構成マネージャーを使用して、SQL Server Reporting Service (SSRS) データベースを更新します。 **データベース** を選択し、**データベースの変更** を選択して新しいサーバー名を使用します。 必ず、SQL Server 2016 用の Reporting Services 構成マネージャーを使用してください。

## <a name="additional-steps-to-install-one-version-service-updates"></a>1 つのバージョンのサービスの更新プログラムをインストールする追加の手順
VHD 環境で 1 つのバージョンのサービスの更新プログラムをインストールするには、次の追加手順が必要です。

### <a name="update-the-azure-storage-emulator"></a>Azure Storage エミュレーター を更新する
Azure Storage エミュレーターを更新し、それが実行されているかどうかを確認します。 **スタート** メニューで、**Microsoft Azure Storage エミュレーター - v4.0** を開き、次のコマンドを実行します。

このコマンドは、エミュレーターを起動します。

```Console
AzureStorageEmulator.exe start
```

このコマンドは、エミュレーターが実行されていることを確認します。

```Console
AzureStorageEmulator.exe status
```

**-server** スイッチまたは **-forcecreate** スイッチを使用して **init**オプションを試してください。 必ず、**new\_name** を新しい名前に置き換えてください。

```Console
AzureStorageEmulator.exe init -server new_name
AzureStorageEmulator.exe init -forcecreate
```

**init** コマンドが失敗した場合、SQL Server Management Studio を使用してストレージ エミュレーター データベースを削除します。 次に、次のコマンドを入力します。

```Console
AzureStorageEmulator.exe init
```

このコマンドを実行すると、次のエラー メッセージが表示される場合があります: "エラー: データベースを作成できません。" ただし、通常、エミュレーターは引き続き起動されます。 エミュレーターを起動するだけでかまいません。

### <a name="update-financial-reporting"></a>財務諸表の更新
1 つのバージョンのサービスの更新プログラムに含まれるスクリプトを使用して、財務報告のためのサーバー名を更新します。 コマンドを取得するには、1 つのバージョンのサービスの更新をダウンロードして展開する必要があります。

管理者として Microsoft Windows PowerShell コマンド ウィンドウを開き、次のコマンドを実行します。 このコマンドには、更新する必要がある既定のパスワードが含まれます。 必ず、**new\_name** を新しい名前に置き換えてください。

```powershell
cd <update folder>\MROneBox\Scripts\Update
.\ConfigureMRDatabase.ps1 -NewAosDatabaseName AxDB -NewAosDatabaseServerName new_name -NewMRDatabaseName ManagementReporter -NewAxAdminUserPassword AOSWebSite@123 -NewMRAdminUserName MRUser -NewMRAdminUserPassword MRWebSite@123 -NewMRRuntimeUserName MRUSer -NewMRRuntimeUserPassword MRWebSite@123 -NewAxMRRuntimeUserName MRUser -NewAxMRRuntimeUserPassword MRWebSite@123
```
