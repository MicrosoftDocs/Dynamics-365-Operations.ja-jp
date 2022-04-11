---
title: Microsoft Dynamics 365 Finance + Operations (on-premises) 環境での Windows Server のアップグレード
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (on-premises) 環境が使用している  Windows Server バージョンをアップグレードする方法について説明します。
author: faix
ms.date: 03/29/2022
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3981dded237d21190dc2d7a952442b2c8dbd56b4
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509684"
---
# <a name="upgrade-windows-server-in-microsoft-dynamics-365-finance--operations-on-premises-environments"></a>Microsoft Dynamics 365 Finance + Operations (on-premises) 環境での Windows Server のアップグレード

このトピックでは、Microsoft Dynamics 365 Finance + Operations (on-premises) 環境で Windows Server バージョンをアップグレードする方法について説明します。

## <a name="prerequisites-for-upgrading-the-sql-server-version"></a>SQL Server バージョンをアップグレードするための前提条件

### <a name="upgrade-from-windows-server-2016-to-windows-server-2019"></a>Windows Server 2016 から Windows Server 2019 へのアップグレード

- Dynamics 365 Finance + Operations (on-premises) 環境は、アプリケーション バージョン 10.0.17 以降である必要があります。
- このローカル エージェントは、バージョン 3.0.0 以降である必要があります。

## <a name="upgrade-active-directory-federation-services"></a>Active Directory フェデレーション サービスのアップグレード

### <a name="upgrade-a-single-ad-fs-instance"></a>単一の AD FS インスタンスのアップグレード

1. ユーザーは発生時に Finance + Operations (on-premises) へサインインできないので、この操作を完了するために十分なダウンタイムをスケジュールします。
1. Active Directory フェデレーション サービス (AD FS) サーバーを開き、次のコマンドを実行します。

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

1. 次の値をメモします: **Active Directory-\>Client ID for AOS application group** および **Active Directory-\>Client ID for Financial Reporting application group**.
1. [Windows Server 2016 から Windows Server 2019 へのアップグレード](/windows-server/upgrade/upgrade-2016-to-2019) のトピックに従って一括アップグレードを実行します。

    > [!NOTE]
    > アップグレード完了後、AD FS ロールを再構成する必要があるという警告メッセージが表示されます。 アプリ グループの再作成に必要な情報を収集したので、この警告は問題ではありません。 ただし、アプリケーションを追加する場合、クライアント ID をバックアップして、後でアプリケーションを再作成する時に再利用できるような方法を使用してください。

1. コンピューターのアップグレードが完了したら、サーバー マネージャーを開き、AD FS のコンフィギュレーションを完了します。
1. [AD FSのコンフィギュレーション](./setup-deploy-on-premises-pu41.md#configureadfs) の手順に従って、AD FS を構成します。 ただし、**Publish-ADFSApplicationGroup.ps1** スクリプトを実行しないでください。
1. 次のコマンドを実行します。

    ```powershell
    # Host URL is your DNS record\host name for accessing the AOS
    .\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -ClientId <"Value of Active Directory->Client ID for AOS application group"> -FinancialReportingClientId <"Client ID for Financial Reporting application group">
    ```

### <a name="upgrade-an-ad-fs-farm"></a>AD FS ファームのアップグレード

Windows 内部データベース (WID) を使用している場合は、[WID データベースを使用した Windows Server 2016 でのAD FS へのアップグレード](/windows-server/identity/ad-fs/deployment/upgrading-to-ad-fs-in-windows-server) の手順に従います。

SQL Server データベースを使用している場合は、[SQL Server を使用した Windows Server 2016 での AD FS へのアップグレード](/windows-server/identity/ad-fs/deployment/upgrading-to-ad-fs-in-windows-server-sql) の手順に従います。

### <a name="create-a-new-ad-fs-farminstance-and-replace-your-old-ad-fs-farminstance"></a>新しい AD FS のファーム/インスタンスを作成し、古い AD FS のファーム/インスタンスを置き換える

1. 新しい AD FS フェデレーション ファーム/インスタンスを作成します。 AD/FS の配置方法の詳細については、[Windows Server AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。
1. [AD FSのコンフィギュレーション](./setup-deploy-on-premises-pu41.md#configureadfs) の手順に従って、AD FS を構成します。 ただし、**Publish-ADFSApplicationGroup.ps1** スクリプトを実行しないでください。
1. 既存の AD FS ファームで、次のコマンドを実行します。

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

1. 次の値をメモします: **Active Directory-\>Client ID for AOS application group** および **Active Directory-\>Client ID for Financial Reporting application group**.
1. 新しい AD FS ファーム/インスタンスで、次のコマンドを実行します。

    ```powershell
    # Host URL is your DNS record\host name for accessing the AOS
    .\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -ClientId <"Value of Active Directory->Client ID for AOS application group"> -FinancialReportingClientId <"Client ID for Financial Reporting application group">
    ```

    新しいファーム/インスタンスを Finance + Operations (On-premises) で使用する準備が整いました。

1. 新しいファーム/インスタンス エンドポイントが古いファーム/インスタンス エンドポイントと異なる場合は、 、**設定の更新** オプションを選択し、**ADFS OpenID メタデータ エンドポイント** フィールドを新しい値に設定して、Microsoft Dynamics Lifecycle Services (LCS) のエンドポイントを更新してください。

## <a name="upgrade-a-node-in-your-service-fabric-cluster"></a>Service Fabric Cluster でのノードのアップグレード

Service Fabric のスタンドアロン クラスターでは、ノードのオペレーティング システムのアップグレードは機械固有の操作です。 (ノードは、仮想コンピューター \[VM\] または物理マシンのいずれかです)。1 つのノードに対してインプレース アップグレードを実行する方法は 2 種類あります。 最初の方法では、アップグレード操作でデータおよびオペレーティング システムのコンフィギュレーションが維持されます。 2 番目の方法では、アップグレード操作でデータおよびオペレーティング システムのコンフィギュレーションは維持されません。 新しいノードを作成し、クラスターに追加することもできます。

このセクションに説明されている方法はすべてクラスターの稼働を維持し、すべてのノードを同時にアップグレードしない場合、サービスの使用に影響を与える可能性はありません。

ノードのアップグレードに使用する方法に関係なく、別のノード タイプに進む前に、ノード タイプ内のすべてのノードをアップグレードしてください。

> [!IMPORTANT]
> クラスターにシード ノードが 3 つしかない場合 (**OrchestratorNodeType**)、一度にアップグレードできるノードは 1 つのみです。 そうしないと、クラスターはシステム サービスを実行し続けられず、クラスターは使用できません。
>
> クラスターにビジネス インテリジェンス (BI)/Management Reporter (MR) ノードが 1 つしかない場合は、アップグレード プロセス中に関連サービスを利用できないので、ダウンタイム ウィンドウにノード アップグレードをスケジュールする必要があります。

### <a name="do-an-in-place-upgrade-that-preserves-operating-system-data"></a>オペレーティング システムのデータを保持するインプレース アップグレードの実行

ノードを無効化し、オペレーティング システムをアップグレードして、すべてのデータを維持するので、この方法は最も簡単なオプションです。 アップグレード後にノードをオンラインに戻す場合は、ノードの有効化が必要です。

1. Service Fabric エクスプローラーで、アップグレードするノードを無効化 (再起動) します。
1. [Windows Server 2016 から Windows Server 2019 へのアップグレード](/windows-server/upgrade/upgrade-2016-to-2019) のトピックに従って一括アップグレードを実行します。
1. ノードのバック アップ後、**Test-D365FOConfiguration.ps1** スクリプトを使用して、アップグレードによって前提条件が既定値に戻っていないことを確認します。 テスト スクリプトで問題が発生する場合は、**Configure-Prereq.ps1** スクリプトと **Complete-Prereq.ps1** スクリプトを実行して修正します。
1. Service Fabric エクスプローラーで、ノードを有効化します。
1. ノードが再び正常になるのを待ち、次のノードに対してこの手順を繰り返します。

### <a name="do-an-in-place-upgrade-that-doesnt-preserve-operating-system-data"></a>オペレーティング システムのデータを保持しないインプレース アップグレードの実行

オペレーティング システムのアップグレード中に、すべてのデータが削除されます。 そのため、ノードには新しいオペレーティング システムがインストールされます。 その後、クラスターに追加し直す前に、各ノードのすべてのコンフィギュレーション手順を完了する必要があります。

1. Service Fabric エクスプローラーで、アップグレードするノードを無効化 (データを削除) します。
1. [ノードの削除](./onprem-remove-reinstall-aos-node.md#remove-a-node) の手順に従って、クラスターからノードを削除します。
1. [Windows Server 2016 から Windows Server 2019 へのアップグレード](/windows-server/upgrade/upgrade-2016-to-2019) のトピックに従って一括アップグレードを実行します。
1. [ノードの削除](./onprem-remove-reinstall-aos-node.md#add-a-node) の手順に従って、ノードをクラスターに追加し直します。
1. ノードをバックアップした後、Service Fabric エクスプローラーで有効にします。
1. ノードが再び正常になるのを待ち、次のノードに対してこの手順を繰り返します。

### <a name="add-new-nodes-to-the-cluster"></a>クラスターへの新しいノードの追加

この方法は前の方法と似ていますが、クラスターから既存のノードを削除する前に新しいノードをスピンアップします。 ノードをダウンさせることができない場合は、この方法によってサービスのパフォーマンスが維持されます。

1. 新しい VM をプロビジョニングします。
1. [ノードの追加](./onprem-remove-reinstall-aos-node.md#add-a-node) の手順に従ってノードを追加します。
1. ノードが追加され、そのノードのサービスが正常に機能した場合、前の手順を繰り返して、追加のノードのプロビジョニング、構成、追加を行います。
1. すべてのノードを追加した後、 [ノードの削除](./onprem-remove-reinstall-aos-node.md#remove-a-node) の手順に従って、古いオペレーティング システムを実行しているノードを削除します。
