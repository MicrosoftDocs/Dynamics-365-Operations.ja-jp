---
title: オンプレミス配置のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。
author: sarvanisathish
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: 79fdb1cef1104bc37461229543bfed514355158c
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850373"
---
# <a name="troubleshoot-on-premises-deployments"></a>オンプレミス配置のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。

## <a name="access-service-fabric-explorer"></a>Service Fabric Explorer へのアクセス

Service Fabric Explorer には、Web ブラウザーと既定のアドレス `https://sf.d365ffo.onprem.contoso.com:19080` を使ってアクセスできます。

アドレスを確認するには、環境の適切なセットアップおよび配置トピックの「DNS ゾーンの作成と A レコードの追加」セクションで使用されていた値をメモします。

- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#createdns)
- [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#createdns)

クライアント証明書が、サイトにアクセスするマシンの証明書、cert:\\CurrentUser\\My に含まれている場合のみ、サイトにアクセスできます (証明書マネージャーで、**証明書 - 現在のユーザー** \> **個人** \> **証明書**に移動します。) サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。

## <a name="monitor-the-deployment"></a>配置の監視

### <a name="identify-the-primary-orchestrator"></a>プライマリ オーケストレータを識別します。

Service Fabric Explorer でローカル エージェントなどのステートフル サービスのプライマリ インスタンスであるマシンを判別するには、**クラスター** \> **アプリケーション** \> **\<*対象のアプリケーションの例*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** を展開します。

プライマリ ノードが表示されます。 ステートレス サービスまたは残りのアプリケーションについては、すべてのノードを確認する必要があります。

次のポイントに注意します。

- OrchestrationService は、Finance and Operations の配置およびサービス アクションを調整します。
- ArtifactsManager は、ファイルを Microsoft Azure クラウド ストレージからローカル エージェント ファイル共有にダウンロードします。 ファイルを必要な形式にも解凍します。

### <a name="review-the-orchestrator-event-logs"></a>オーケストレータ イベント ログを確認

イベント ビューアー内の プライマリ OrchestrationService オーケストレータ マシンから、 **アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent** と移動します。

> [!NOTE]
> 完全なエラー メッセージを表示するには、 **詳細** タブを選択してください。

次のモジュールがインストールされます:

- 共通
- ReportingServices
- AOS
- FinancialReporting

次のコマンドを実行する必要があります。

- **セットアップ**
- **Dvt** – このコマンドは配置検証テストを実行します。
- **Cleanup** – このコマンドは環境のサービスと削除に使用されます。

次のフォルダには、追加の情報が含まれます。

- AX-SetupModuleEvents
- AX-SetupInfrastructureEvents
- AX-BridgeService

イベント ビューアーで Microsoft Dynamics エントリを確認するには、次の手順を実行します。

1. イベント ビューアーで **カスタム ビュー** を右クリックして、**カスタム ビューの作成** を選択します。

    ![カスタム表示の作成](media/Create-Custom-View.png)

2. **イベント ログ** フィールドで **Dynamics** を選択します。

    ![Dynamics の選択](media/Select-Dynamics.png)

> [!NOTE]
> また、**カスタム ビュー** で **管理イベント** も確認してください。

### <a name="service-fabric-explorer"></a>Service Fabric Explorer

クラスタ、アプリケーション、およびノードの状態に注意してください。 Service Fabric Explorer にアクセスする方法については、[Service Fabric Explorer にアクセスする](troubleshoot-on-prem.md#access-service-fabric-explorer)を参照してください。

#### <a name="error-partition-is-below-target-replica-or-instance-count"></a>エラー、「パーティションがターゲット レプリカまたはインスタンス数を下回っています」

次のエラーが表示される場合があります。

> パーティションがターゲット レプリカまたはインスタンス数を下回っています

このエラーはルート エラーではありません。 各ノードのステータスが準備できていないことを示します。 AXSFType (AOS) では、ステータスがまだ **InBuild** である可能性があります。

エラー メッセージに関連するコンピューターで、イベント ビューアーを使用して最新の活動を表示します。

#### <a name="axsftype"></a>AXSFType

AXSFType (AOS) に **InBuild** のステータスが表示される場合、DB Sync ステータスおよび Application Object Server (AOS) コンピューターからの他のイベントを確認してください。

エラーを診断するには、イベント ビューアーを使用して次のイベント ログを確認します。

- アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DatabaseSynchronize
- カスタム ビュー \> 管理イベント

#### <a name="error-extractinstallerservice-failed-to-extract-cusersdynusercontosoappdatalocaltemp1blssblhw0nfabricinstallerservicecodefabricclientdll"></a>エラー: "'ExtractInstallerService は抽出に失敗しました' C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll"

次のエラーが表示される場合があります。

> "ExtractInstallerService は抽出に失敗しました" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll。

このエラーが発生した場合は [Azure Service Fabric](https://go.microsoft.com/fwlink/?LinkId=730690) の最新バージョンをダウンロードしてください。 エラー メッセージのユーザー名およびパスは、環境によって変化することに注意してください。

#### <a name="service-fabric-logs"></a>Service Fabric ログ

Service Fabric アプリケーションのさらなる詳細については、C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log のログ ファイルを参照してください。

### <a name="lifecycle-services"></a>Lifecycle Services

Microsoft Dynamics Lifecycle Services (LCS) で環境のに対する現在の配置ステータスに注意してください。

## <a name="a-time-out-error-occurs-when-a-service-fabric-cluster-is-created"></a>Service Fabric cluster の作成時にタイムアウト エラーが発生する

該当するセットアップ トピックの "スタンドアロン Service Fabric Cluster のセットアップ" セクションおよび環境の配置トピックに記載されているように Test-D365FOConfiguration.ps1 を実行します。 エラーに注意してください。

- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#setupsfcluster)
- [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)

これらの手順を必ず実行してください。

- すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。
- Service Fabric Server 証明書にすべての Service Fabric ノード上にネットワーク サービス用アクセス制御リスト (ACL) が含まれていることを確認します。
- [環境設定](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) で記載されているウイルス対策の除外を確認します。

## <a name="a-time-out-error-occurs-while-youre-waiting-for-installer-service-to-be-completed-for-machine-xxxx"></a>インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウト エラーが発生する

インターネット プロトコル (IP) アドレスごとに (つまり、コンピューターごとに) 1 つのノード タイプがサポートされます。 ノードが同じマシン上で再利用されているかどうかを確認してください。 たとえば、AOS および ORCH は、同一のマシン上に存在してはならず、ConfigTemplate.xml が正しく定義されている必要があります。

## <a name="remove-a-specific-application"></a>特定のアプリケーションを削除

配置の削除またはクリーンアップに LCS を使用することをお勧めします。 ただし、必要に応じて、アプリケーションを削除する Service Fabric Explorer を使用することもできます。

Service Fabric エクスプローラーで、**アプリケーション ノード** \> **アプリケーション** \> **MonitoringAgentAppType-Agent** に移動します。 **ファブリック:/エージェント監視** の横にある省略記号ボタン (**...**) を選択し、アプリケーションを削除します。 アプリケーションの完全な名前を入力して、アプリケーションの削除を確認します。

また、省略記号ボタンの選択および**非引当タイプ**の順に選択することにより、MonitoringAgentAppType-Agent を削除することができます。 アプリケーションの削除を確認するために、正式名称を入力します。

## <a name="remove-all-applications-from-service-fabric"></a>Service Fabric からすべてのアプリケーションを削除

次のスクリプトは、LocalAgent および LocalAgent の監視エージェントを除く、すべての Service Fabric アプリケーションを削除してプロビジョニング解除します。 オーケストレータ仮想マシン (VM) 上でこのスクリプトを実行する必要があります。

```powershell
$applicationNamesToIgnore = @('fabric:/LocalAgent', 'fabric:/Agent-Monitoring')
$applicationTypeNamesToIgnore = @('MonitoringAgentAppType-Agent', 'LocalAgentType')

Get-ServiceFabricApplication | `
    Where-Object { $_.ApplicationName -notin $applicationNamesToIgnore } | `
    Remove-ServiceFabricApplication -Force

Get-ServiceFabricApplicationType | `
    Where-Object { $_.ApplicationTypeName -notin $applicationTypeNamesToIgnore } | `
    Unregister-ServiceFabricApplicationType -Force
```

## <a name="remove-service-fabric"></a>Service Fabric の削除

Service Fabric クラスターを完全に削除するには、以下の手順に従います。

1. 次のコマンドを実行します。

    ```powershell
    .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

2. エラーが発生した場合は、**CleanFabric.ps1**コマンドを使用して、クラスタ内の特定のノードを削除します。 このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。
3. 既定の場所を使用している場合、**C:\\ProgramData\\SF** フォルダーを削除します。 それ以外の場合、指定したフォルダーを削除します。

    "アクセス拒否" エラーが発生した場合は、Microsoft Windows PowerShell を再起動するか、マシンを再起動します。

## <a name="clean-up-an-existing-environment-and-redeploy"></a>既存環境のクリーンアップと再配置

既存の環境をクリーンアップして再配置するには、以下の手順を実行します。

1. LCS でプロジェクトを開き、**環境**セクションで展開を削除します。

    アプリケーションが環境の Service Fabric Explorer から表示されなくなります。 このプロセスは 1、2 分かかります。

2. LocalAgentCLI.exe を含むオーケストレーター マシンにアクセスし、次の手順に従います。

    1. ローカル エージェント クリーンアップを実行します。

        ```powershell
        .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
        ```

    2. Service Fabric を削除します。

        ```powershell
        .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath '<path of ClusterConfig.json>'
        ```

    3. ノードが失敗した場合、**CleanFabric.ps1** コマンドを実行してください。 このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。
    4. すべての Service Fabric ノードの **C:\\ProgramData\\SF\\** フォルダーを削除します。

        "アクセス拒否" エラーが発生した場合は、マシンを再起動してからもう一度実行します。

3. 必要に応じて証明書を削除または更新します。

    すべての AOS、BI、ORCH、および DC ノードから古い証明書を削除します。

    - 証明書は、次の証明書ストアに存在します: Cert:\\CurrentUser\\My\\、Cert:\\LocalMachine\\My, and Cert:\\LocalMachine\\Root。
    - Microsoft SQL Server の設定が変更される場合は、SQL Server 証明書を削除します。
    - Active Directory フェデレーション サービス (AD FS) の設定が変更される場合は、AD FS 証明書を削除します。

4. 必要に応じて、次の構成ファイルを更新します。

    - ConfigTemplate.xml
    - ClusterConfig.json

    テンプレートのフィールドに正しく入力する方法については、ご使用の環境に適した設定と配置のトピックを参照してください。

    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md)

5. LCS でプロジェクトを開き、必要に応じて LCS のオンプレミス コネクタを更新します。

    1. 環境の LCS オンプレミス コネクタを再作成するか、または既存のコネクタの設定を編集します。

        LCS の値を簡単にコピーするには、.\\Get-AgentConfiguration.ps1 script を使用します。

    2. 最新のローカル エージェント コンフィギュレーション、localagent config.json をダウンロードします。

6. 環境に適したセットアップと展開のトピックで次の指示に従って、再度展開します。

    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md)。

## <a name="find-the-local-agent-values-that-are-used"></a>使用するローカル エージェント値の検索

Service Fabric Explorer でローカル エージェント値を見つけることができます。 **クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent** に移動して **詳細** を選択します。

または、次の Windows PowerShell コマンドを実行します。

```powershell
.\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

## <a name="install-upgrade-or-uninstall-a-local-agent"></a>ローカル エージェントのインストール、アップグレード、アンインストール

ローカルエージェントを更新する方法については、 [ローカルエージェントを更新する](../lifecycle-services/update-local-agent.md) を参照してください。

また、以下のアップグレードおよびアンインストール コマンドを使用することができます:

```powershell
LocalAgentCLI.exe Install <path of localagent-config.json>
LocalAgentCLI.exe Cleanup <path of localagent-config.json>
```

> [!NOTE]
> **クリーンアップ** コマンドはファイル共有に配置された一切のファイルを削除しません。 ファイル共有は再利用できます。

## <a name="an-error-occurs-when-local-agent-services-are-started"></a>ローカル エージェント サービスを開始される際にエラーが発生

ローカル エージェント サービスが開始されると、次のエラーが表示される場合があります。

> ファイル、アセンブリ 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35'、もしくはその依存関係の 1 つをロードできませんでした。

このエラーは厳密な名前検証が有効になっていることを意味します。 Configure-PreReqs.ps1 を使用して、この確認をオフにすることができます。 厳密な名前検証がもう有効になっていないことを確認するには、Test-D365FOConfiguration.ps1 を実行します。

## <a name="a-validation-in-progress-message-is-shown-for-several-minutes-in-lcs"></a>「検証が進行中」のメッセージが LCS に数分表示

ローカル エージェントの検証に関する一般的な問題をトラブルシューティングするには、次の手順を実行します。

1. コンピューターを正しくコンフィギュレーションするすべてのオーケストレータ機械で **Configure-PreReqs.ps1** を実行します。
2. Test-D365FOConfiguration.ps1 スクリプトがすべてのオーケストレータ マシンで通ることを確認します。
3. LocalAgentCLI.exe のインストールが正常に完了したことを確認します。
4. Service Fabric Explorer で、すべてのアプリケーションが正常であることを確認します。
5. アプリケーションが正常でない場合は、障害が発生しているサービスのプライマリ ノードを探します。 イベント ビューアーでは、次の場所でのイベントを検索します。

    - カスタム ビュー \> 管理イベント
    - アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-LocalAgent

## <a name="local-agent-errors"></a>ローカル エージェント エラー

### <a name="issue"></a>出庫

**エラー:** 次のエラーが表示される場合があります:

> コマンドを処理できません

> チャンネル情報を取得できません

> ホスト プロセスがクラッシュする処理されない例外が原因で RunAsync が失敗しました: System.ArgumentNullException: 値を null にすることはできません。 パラメーター名: 証明書

**理由:** これらのエラーは OnPremLocalAgent 証明書に指定された証明書が有効でないか、またはテナントに対して正しく構成されていないために発生することがあります。

**ステップ:** エラーを解決するには、次の手順に従います。

1. すべてのオーケストレータ ノードで **Test-D365FOConfiguration.ps1** を実行し、すべてのチェックに合格することを確認します。
2. ローカル エージェント コンフィギュレーションに指定された証明書が正しいことを確認します。

    - LCS および ConfigTemplate.xml ファイルで指定する拇印に特殊文字がないことを確認します。
    - 証明書は、infrastructure\\ConfigTemplate.xml の次のセクションで指定されているものと同じ証明書である必要があります。

        ```xml
        <Certificate type="Orchestrator" exportable="true" generateSelfSignedCert="true">
            <Name>OnPremLocalAgent</Name>
            <Thumbprint></Thumbprint>
            <ProtectTo></ProtectTo>
        </Certificate>
        ```

3. LCS のローカル エージェント コンフィギュレーションで指定される同じ証明書が、環境に対する適切な設定および配置トピックの「テナント用 LCS 接続の構成」セクションで手順の完了に使用されたことを確認します。

    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#configurelcs)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

4. ローカル エージェントをアンインストールします。
5. ローカル エージェント コンフィギュレーションで正しい証明書を指定し、もう一度コンフィギュレーション ファイルをダウンロードします。
6. 新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。

### <a name="error"></a>エラー

**エラー:** サービス中に "資産をダウンロードできません" というエラーが表示され、詳細に "パッケージに提供された資格情報が認識されません" と表示されます。

**理由:** ACL が証明書で正しく定義されていません。

**ステップ:**

オーケストレータ マシンのクライアント証明書から ACL が削除されたかを確認します。 オーケストレータ マシンの .\Test-D365FOConfiguration.ps1 スクリプトを実行し、ACL を確認します。

エラーを解決するには、.\Set-CertificateAcls.ps1 スクリプトを実行して ACL をリセットします。 

### <a name="error"></a>エラー

**エラー:**

> パス '\\...\\agent\\assets\\StandAloneSetup-76308-1.zip' へアクセスすることは、拒否されます。

**理由:** ローカル エージェント コンフィギュレーションで指定されたファイル共有が無効です。

**ステップ:** エラーを解決するには、次の手順に従います。

1. 指定した共有が存在することを確認します。
2. ローカル エージェント ユーザーが共有への完全なアクセス許可を持っていることを確認します。 ローカル エージェント ユーザーは、次のセクションの ConfigTemplate.xml で指定されるドメイン ネーム システム (DNS) 名です。

    ```xml
    <ADServiceAccount type="gMSA" name="svc-LocalAgent$" refName="gmsaLocalAgent">
        <DNSHostName>svc-LocalAgent.d365ffo.onprem.contoso.com</DNSHostName>
    </ADServiceAccount>
    ```

3. 適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックが完了したことを確認します。

    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#setupfile)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupfile)

4. ローカル エージェントをアンインストールします。
5. ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。
6. 新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。

### <a name="error"></a>エラー

**エラー:** サービス操作を行うと次のエラーが表示されます:

> コマンドの抽出セットアップ フォルダーを取得できません

**理由:** そのファイル共有は削除または変更されました。

**手順:** ファイル共有の設定内容を確認するには、Microsoft SQL Server Management Studio を開いてオーケストレータ データベースで次のクエリを実行します:

```
select * from OrchestratorCommandArtifact where CommandId = 'xxx'
```

### <a name="error"></a>エラー

**エラー:**

> ユーザー 'D365\\svc-LocalAgent$' へのログインが失敗しました。 理由: 指定した名前に一致するログインが見つかりませんでした。 \[CLIENT: 10.0.2.23\]

**理由:** ローカル エージェント ユーザーはオーケストレーション データベースに接続できません。 ユーザーが削除され、Active Directory ドメイン サービス (AD DS) に再作成されているために、この問題が発生する可能性があります。 したがって、ユーザーのセキュリティ識別子 (SID) が変更され、SQL Server インスタンスまたはデータベースのユーザーに与えられたアクセスは機能しなくなります。

**ステップ:** エラーを解決するには、次の手順に従います。

1. SQL Server インスタンスで次のスクリプトを実行します。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    このスクリプトは、空のデータベースがまだ存在していない場合に、空のオーケストレータ データベースを作成します。 ローカル エージェント ユーザーをデータベースに追加し、データベース\_アクセス許可の所有者に渡します。

    適切なアクセス許可が付与された後、アプリケーションは自動的に正常な状態になります。

2. SQL Server インスタンスの完全修飾ドメイン名 (FQDN)、データベース名、ローカル エージェント ユーザーなどの設定が LCS で間違って提供された場合は、設定を変更し、ローカル エージェントを再インストールします。

上記の手順でエラーが解決しない場合は、SQL Server インスタンスとデータベースからローカル エージェント ユーザーを手動で削除し、Initialize-Database スクリプトを再実行します。

AD DS でユーザーを再作成する場合、SID が変更されることに注意してください。 この場合、ユーザーの以前の SID を削除し、新しい SID を追加します。

### <a name="error"></a>エラー

**エラー:** 
> データベースを移行できません

**ステップ:**

- SQL Server リスナーへのアクセスがあることを確認します。
- テストをしている場合は、最初からやり直して空のオーケストレータ データベースを使用できます。

### <a name="issue"></a>問題点

[データベースを構成する](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configuredb) プロシージャを実行するときに SQL Server インスタンスが名前付きインスタンスの場合は、**-DatabaseServer \[FQDN/Instancename\]** パラメーターを使用します。

### <a name="issue"></a>問題点

ローカル エージェント ユーザーは、SQL Server インスタンスまたはデータベースに接続できません。

**ステップ:** エラーを解決するには、次の手順に従います。

1. SQL Server のプライマリ ノード データベースから svc-LocalAgent ユーザーを削除し、両方のサーバーからログインを削除します。
2. 次のスクリプトを実行します。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    > [!IMPORTANT]
    > これらのスクリプトは、**常時オン**に設定されているときは機能しません。 データベースは最初にプライマリ ノードに作成されてから複製される必要があります。

### <a name="error"></a>エラー

**エラー:**

> RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。 ---\> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'

**理由:** ローカル エージェント マシンは lcsapi.lcs.dynamics.com に接続できません。 「リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'」に対する AX-BridgeService イベント ログを確認します。

**ステップ:** エラーを解決するには、次の手順に従います。

1. **psping lcsapi.lcs.dynamics.com:80** を実行します。
2. 前述のコマンドから応答を受信しない場合は、組織の IT 部門に問い合わせます。 ファイアウォールが lcsapi へのアクセスをブロックしているか、もしくはプロキシの問題が発生しています。

    ```
    lcsapi.lcs.dynamics.com:443
    login.windows.net:443
    uswelcs1lcm.queue.core.windows.net:443
    www.office.com:443
    login.microsoftonline.com:443
    dc.services.visualstudio.com:443
    uswelcs1lcm.blob.core.windows.net:443
    uswedpl1catalog.blob.core.windows.net:443
    ```

## <a name="restart-applications-such-as-aos"></a>アプリケーション (AOS など) を再起動

Service Fabric で、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード**の順に展開します。 省略記号ボタン (**...**) を選択し、**再起動**を選択します。 求められたらコードを入力します。

## <a name="upgrade-service-fabric"></a>Service Fabric を更新します。

Service Fabric Explorer は次のようなメッセージを表示します:

> 問題のあるイベント: SourceId=「System.UpgradeOrchestrationService」、プロパティ =「ClusterVersionSupport」、HealthState=「警告」、ConsiderWarningAsError=false。
現在のクラスタ バージョン 6.1.467.9494 のサポートは、5/30/2018 12:00:00 AM に終了します。 Get-ServiceFabricRegisteredClusterCodeVersion を使用して利用可能なアップグレードを表示し、Start-ServiceFabricClusterUpgrade を使用してアップグレードしてください。

最小要件が 1 つの Microsoft SQL Server Reporting Services (SSRS) ノードと 1 つの Management Reporter ノードであるため、PreUpgradeSafetyCheck をスキップするパラメータを渡す必要があります。

Windows PowerShell で Service Fabric をアップグレードするにはこれらの手順に従います。

1. Service Fabric Cluster に接続します。 次のコマンドで **123** をサーバー / スター拇印に置き換えて、適切な IP アドレスを使用します。

    ```powershell
    Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123
    ```

2. ダウンロードされた最新バージョンを取得します。

    ```powershell
    Get-ServiceFabricRegisteredClusterCodeVersion
    ```

3. アップグレードを開始します。 **-CodePackageVersion** には、最新バージョンを入力します。

    > [!NOTE]
    > **-UpgradeReplicaSetCheckTimeout** は SSRS と Management Reporter の PreUpgradeSafetyCheck をスキップするために使用します。 詳細については、[Service Fabric サービスのアップグレードが動作しない](https://github.com/Azure/service-fabric-issues/issues/595) を参照してください。 **UpgradeDomainTimeoutSec 600 UpgradeTimeoutSec 1800** を使用することもできます。 詳細については、[アプリケーション アップグレード パラメーター](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters) を参照してください。

    ```powershell
    Start-ServiceFabricClusterUpgrade -Code -CodePackageVersion 6.1.472.9494 -Monitored -FailureAction Rollback -UpgradeReplicaSetCheckTimeout 30
    ```

4. アップグレードの状態を取得します。

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

詳細については、[アプリケーション アップグレードのトラブルシューティング](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)を参照してください。

新しい Service Fabric リリースの時期については、[Azure Service Fabric チームのブログ](https://blogs.msdn.microsoft.com/azureservicefabric/) を参照してください。

アップグレード後に Service Fabric Explorer で警告が表示された場合は、ノードを記録して、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード** を展開して再起動してください。 省略記号ボタン (**...**) を選択し、**再起動**を選択します。
 
## <a name="error-unable-to-load-dll-fabricclientdll"></a>エラー、「DLL 'FabricClient.dll' を読み込むことができません」

"DLL 'FabricClient.dll' をロードできません" というエラーが表示された場合は、Windows PowerShellを 閉じて再起動してください。 エラーが引き続き発生する場合は、コンピューターを再起動します。

## <a name="what-cluster-id-should-be-used-in-the-agent-configuration"></a>エージェント コンフィギュレーションでどのようなクラスター ID を使用する必要がありますか。

クラスタ ID は、任意のグローバル一意識別子 (GUID) です。 この GUID は、追跡目的で使用されます。

## <a name="encryption-errors"></a>暗号化エラー

暗号化エラーの例は "AXBootstrapperAppType"、"Bootstrapper"、"AXDiagnostics"、"RTGatewayAppType"、"ゲートウェイの潜在的なエラー関連"、 "Microsoft.D365.Gateways.ClusterGateway.exe" を含みます。

AOS アカウント パスワードを暗号化するために使用されたデータ暗号化証明書がマシンにインストールされていない場合、これらのエラーのいずれかが発生することがあります。 この証明書が証明書 (ローカル コンピューター) に含まれているか、プロバイダーの種類が正しくない可能性があります。

エラーを解決するには、credentials.json ファイルを検証します。 次のコマンドを (AOS1 上で) 入力することにより、テキストが正しく復号化されていることを確認します。

```powershell
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

このエラーも、**''** パラメーターが ApplicationManifest ファイルで定義されていない場合にも発生させることができます。 イベント ビューアーで、このパラメータが定義されているどうかを確認するには、**カスタム ビュー** \> **管理イベント**の順に移動し、次の情報を確認します。

- Credentials.json ファイルの資格情報の暗号化には、正しいレイアウト/構造があります。 詳細については、ご使用の環境に適した設定および配置のトピックの「資格情報の暗号化」のセクションを参照してください。

    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#encryptcred)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#encryptcred)

- 決算引用符が線の終わりまたは次の線に表示されます。

イベント ビューアーの **カスタム ビュー** \> **管理イベント** で、**Microsoft-Service Fabric** ソース カテゴリのエラーに注意します。

## <a name="properties-to-create-a-dataencryption-certificate"></a>DataEncryption 証明書を作成するためのプロパティ

DataEncryption 証明書を作成するのにには、次のプロパティを使用します。

- **自己署名証明書** – このパラメータは、自己署名証明書を使用する場合にのみ有効にします。
- **証明書の目的** – この証明書のすべての目的を有効にします。
- **署名アルゴリズム** – **sha256RSA** を指定してください。
- **署名ハッシュ アルゴリズム** – **sha256** を指定してください。
- **発行者** – 指定 **CN = DataEncryptionCertificate**。
- **公開キー** – **RSA (2048 ビット)** を指定します。
- **Thumbprint アルゴリズム** – **sha1** を指定します。

> [!WARNING]
> 実稼働環境では、自己署名証明書を使用しないでください。 代わりに、証明書機関によって発行された証明書を使用します。

## <a name="the-certificate-and-private-key-that-should-be-used-for-decryption-cant-be-found-0x8009200c"></a>暗号の解読に使用すべき証明書と秘密キーを見つけることができません (0x8009200C)

証明書と ACL がない、または間違った拇印の入力がある場合は、特殊文字をチェックし、C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt で拇印を探します。

次のコマンドを使用して暗号化されたテキストを検証することもできます。

```
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACLs を確認してください。

credentials.json ファイルが変更された場合は、LCS から環境を削除して再配置します。

上記のソリューションのいずれも機能しない場合は、次の手順を実行します。

1. ConfigTemplate.xml ファイルで指定されたドメイン名と Active Directory アカウント名が正しいことを確認します。
2. 用意されたスクリプトを使用して証明書が生成されなかった場合に ConfigTemplate.xml ファイルで指定された拇印が正しいことを確認します。
3. LCS で指定された証明書の拇印が正しく、ConfigTemplate.xml で指定されたものと拇印が一致することを確認します。 特殊文字がないことを確認します。 **.\\Get-DeploymentSettings.ps1** を実行して、コピーしやすい方法で拇印を取得することができます。
4. 証明書が自己生成されない場合、プロバイダー名が次の証明書タイプと一致することを確認してください。

    - **ServiceFabricEncryption type:** Microsoft Enhanced Cryptographic Provider v1.0
    - **その他のすべての証明書タイプ:** Microsoft の拡張された RSA および AES 暗号化プロバイダー

5. Set-CertificateAcls.ps1 および Test-D365FOConfiguration.ps1 スクリプトがすべての Service Fabric マシンで正常に実行されたことを確認します。
6. Credentials.json ファイルが存在し、エントリが適切な値に復号化されるよう確認します。

    AOS マシンのいずれかで、データの暗号化証明書が正しいことを確認する次のコマンドを実行します。

    ```powershell
    Invoke-ServiceFabricDecryptText '<encrypted string>' -StoreLocation LocalMachine
    ```

7. いずれかの証明書を変更する必要がある場合、もしくは構成が正しくない場合は、次の手順を実行してください:

    1. **ConfigTemplate.xml** ファイルを編集して、正しい値が出るようにします。
    2. すべてのセットアップ スクリプトと **Test-D365FOConfiguration** スクリプトを実行します。

8. LCS で環境を再構成します。

## <a name="management-reporter"></a>Management Reporter

追加のログは、プロバイダーを登録することで実行できます。 [ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) を **プライマリ**オーケストレータ マシン にダウンロードし、次のコマンドを実行します。 プライマリ インスタンスであるマシンを判別するには、Service Fabric Explorerで、**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** の順に展開します。

> [!NOTE]
> イベント ビューアーの結果が正しく表示されない場合 (たとえば、単語が切り詰められた場合など)、最新のマニフェストおよび .dll ファイルを取得してください。 最新のマニフェストと .dll ファイルを取得するには、エージェント ファイル共有の WP フォルダに移動します。 この共有は、適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックで作成されました。
> 
> - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#setupfile)
> - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupfile)
> 
> **例:** \[*エージェント共有*\]\\wp\\\[*配置名*\]\\StandaloneSetup-...\\アプリ\\ ETWManifests

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"}
```

プロバイダーの登録を解除する必要がある場合は、次のコマンドを使用します。

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"} -Unregister
```

プロバイダーが登録されると、新しい配置についての追加詳細は**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** でイベント ビューアーにログインされます。 次のフォルダが表示されます:

- MR-Logger
- MR-Sql

新しいフォルダーを表示するには、イベント ビューアーを終了して、再表示する必要があります。 追加の詳細を表示するには、もう一度環境を配置する必要があります。

### <a name="an-error-occurs-while-addaxdatabasechangetracking-is-running"></a>AddAXDatabaseChangeTracking の実行中に発生するエラー

Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet) で AddAXDatabaseChangeTracking を実行しているときにエラーが発生した場合は、フル パスが正しいことを確認してください。 フル パスの例は **ax.d365ffo.onprem.contoso.com** です。

スター証明書での問題が原因でエラーが発生する可能性もあります。 たとえば、リモート証明書 CN=\*.d365ffo.onprem.contoso.com には、無効な、またはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。

### <a name="run-the-initialize-database-script-and-validate-that-databases-have-correct-users"></a>データベース初期化スクリプトを実行し、データベースのユーザーが適切であることを検証

AddAXDatabaseChangeTracking イベントのみを受け取った場合は、`https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService` にアクセスし、Finance and Operations の MetadataService サービスにアクセスしてみてください。

次に、wif.config ファイルでサービスの証明書を確認します。 ファイルを検索するには、AOS マシンにサインインし、タスク マネージャーで **AxService.exe** を探してください。 TimeZonePatcherを右クリックし、 **ファイルの場所を開く** を選択します。 wif.config ファイルでは、3 つの拇印を確認する必要があります。 これらの拇印に関する次の要件に注意してください。

- これらは異なる必要があります。
- これらは、この順序である必要があります。

    1. Financialreportingの拇印
    2. ReportingServiceの拇印
    3. SessionAuthenticationの拇印

拇印がこれらの要件の両方を満たしていない場合は、正しい拇印を使用して LCS から再配置をする必要があります。

### <a name="the-remote-name-cant-be-resolved"></a>リモート名を解決できません

**エラー:**

> リモート名を解決できませんでした。'x.d365fo.onprem.contoso.com' / メッセージを承認できなかった `https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService` をリッスンしていたエンドポイントはありませんでした。

**理由:** この問題は、通常正しくないアドレスまたは SOAP アクションによって引き起こされます。

**手順:** URL を手動で開き、アドレスにアクセスできることを確認します。 詳細については、イベント ビューアーで [InnerException] のテキストが存在するかどうか確認してください。

### <a name="error-on-importdefaultreports"></a>ImportDefaultReports のエラー

配置中に Management Reporter レポートがチェックアウトされると、配置処理は失敗します。 レポートがチェック アウトされているかどうかを表示するには、FinancialReporting データベースで次の**選択**明細書を実行します。

```
select checkedoutto, * from Reporting.ControlReport where checkedoutto is not null
select checkedoutto, * from Reporting.ControlRowMaster where checkedoutto is not null
select checkedoutto, * from Reporting.ControlColumnMaster where checkedoutto is not null
```

どのユーザーがオブジェクトをチェック アウトするかを知るには、次の**選択**ステートメントを実行します。

```
select * from Reporting.SecurityUser where UserID = ''
```

この問題を手動で解決するには、以下のテーブルを次のコマンドを使用して更新し、 **checkedoutto** を **null** に設定します。

```
update Reporting.ControlReport set checkedoutto = null where checkedoutto is not null
update Reporting.ControlRowMaster set checkedoutto = null where checkedoutto is not null
update Reporting.ControlColumnMaster set checkedoutto = null where checkedoutto is not null
```

## <a name="axdbadmin-cant-connect-to-the-database-server-sql-lscontosocom"></a>axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。

**理由:** AXDB データベースに接続するためのアクセス許可がありません。

**ステップ:**

1. 既に存在する場合は、データベースから axdbadmin ユーザーを削除します。
2. **ConfigTemplate.xml** ファイルで、AXDB データベースに追加する必要があるユーザー名を指定してください。

    ```xml
    <Security>
        <User refName="axdbadmin" type="SqlUser" userName="axdbadmin" />
    </Security>
    ```

3. axdbadmin ユーザーを追加するには、もう一度初期化データベース スクリプトを実行します。

## <a name="unable-to-resolve-the-xpath-value"></a>xPath 値を解決することができません。

予想される動作では、次の **xPath** 値を解決することはできません。 

\[TopologyInstance/CustomizationGroup\[@name='ServiceConfiguration'\]/Group\[@name='AOSServicePrincipalUser'\]/Customizations/Customization\[@fieldName='PrincipalUserAccountPassword'\]/@selectedValue

したがって、 **xPath** の値が解決できないことは問題ではありません。 **xPath** 値は、AOS ランタイム ユーザーの情報を検索します。 ただし、セキュリティが統合されているため、その情報は必要ありません。 別の理由でエラーを調査する必要がある場合は、 **xPath** の値を解決できないと通知されます。

## <a name="ad-fs"></a>AD FS

### <a name="the-sign-in-page-doesnt-redirect-you"></a>サインイン ページにリダイレクトされません。

サインイン ページにはリダイレクトされない可能性がありますが、資格情報の確認を続行します。 また、リダイレクトの可能性がありますが、次のメッセージが表示されます。

> エラーが発生しました。 詳細については、システム管理者に問い合わせてください。

そのような場合、問題を解決するには、次の手順を実行します。

- AD FS リンクを信頼されているサイトの一覧に追加します。
- Dynamics 365 リンクを信頼されているサイトの一覧に追加します。
- 末尾にスラッシュ「/」を追加し、動作が変更されるかどうかを確認します。

**ADFS** \> **アプリケーション グループ**の順に移動して、AD FS マネージャーを確認します。 **Microsoft Dynamics 365 for Operations オンプレミス**をダブルクリックします。 その後、**ネイティブ アプリケーション**で、**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション**をダブルクリックします。

**リダイレクト URI** 値に注意してください。 Finance and Operations の DNS 前方参照ゾーンに一致させる必要があります。

### <a name="error-could-not-establish-trust-relationship-for-the-ssltls-secure-channel"></a>エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」

「SSL/TLS のセキュリティで保護されているチャネルに対する信頼関係を確立できませんでした」というエラーが表示された場合は、次の操作を行います。

1. Service Fabric で、**クラスタ** \> **アプリケーション** \> **AXSFType** \> **fabric:/AXSF** の順に移動し、**詳細**タブでスクロールし、**Aad\_AADMetadataLocationFormat** および **Aad\_FederationMetadataLocation** の URL に注意します。
2. AOS からそれらの URL を参照します。
3. 詳細については、AOS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** の順に移動します。
4. AD FS 証明書が信頼されていることを確認します。

    1. AD FS 証明書を確認します。 AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理**に移動します。
    2. **AD FS** \> **サービス** \> **証明書** を展開し、証明書を記録しておきます。 たとえば、1 つの証明書は、dc1.contoso.com の場合があります。
    3. AOS マシンの、Microsoft 管理コンソール証明書スナップインで、**証明書 (ローカル コンピューター)** \> **信頼済ルート証明機関** \> **証明書**の順に移動し、AD FS 証明書が一覧表示されていることを確認します。

サイトが安全でないことを示すメッセージが表示された場合は、AD FS の Secure Sockets Layer (SSL) 証明書が信頼済ルート証明機関ストアに追加されていません。

### <a name="you-cant-connect-to-the-remote-server-in-some-locations"></a>一部の地域ではリモート サーバーに接続できません

次の場所でリモート サーバーに接続できない場合があります。

- System.Net.HttpWebRequest.GetResponse()
- System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)
- System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)

この場合は、エラーの受信元である C: \\ProgramData\\SF\\AOS\_1\\Fabric\\work\\Applications\\AXSFType\_App35\\ ログ フォルダーに移動し、出力ファイルを確認してください。 out ファイルには、次の情報が含まれます。

> System.Net.WebException: リモート サーバーに接続できません ---\>
>
> System.Net.Sockets.SocketException: 接続した当事者が一定時間適切に応答しなかったため接続試行に失敗したか、接続したホストが x.x.x.x:443 に応答できなかったため確立された接続に失敗しました

Psping を使用してリモート サーバーに対する接続を試みることもできます。 Psping の詳細については、[Psping](/sysinternals/downloads/psping) を参照してください。

### <a name="redirect-sign-in-questions-and-issues"></a>サインイン時の質問および問題をリダイレクト

サインイン時に問題が発生した場合は、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。 次に例を示します。

- **プロビジョニング \_AdminPrincipalName**: `AXServiceUser@contoso.com`
- **プロビジョニング\_AdminIdentityProvider**: `https://DC1.contoso.com/adfs`

値が有効でない場合は、処理を続行できず、LCS から再配置する必要があります。

Reset-DatabaseUsers.ps1 を使用した場合、変更内容を有効にする前に、Dynamics サービスを再起動する必要があります。 引き続きサインインの問題がある場合は、USERINFO テーブルで、**NETWORKDOMAIN** および **NETWORKALIAS** の値を記録してください。 次に例を示します。

- **NETWORKDOMAIN:** `https://DC1.contoso.com/adfs`
- **NETWORKALIAS:** `AXServiceUser@contoso.com`
- **IDENTITYPROVIDER:** これは **NETWORKDOMAIN** の内容と一致している必要があります。

AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理** \> **サービス**に移動します。 **フェデレーション サービス プロパティの保守と編集** を右クリックします。 **フェデレーション サービスの識別子** は **USERINFO.NETWORKDOMAIN** の値と一致している必要があり、URL に **https** が入っている必要があります (たとえば `https://DC1.contoso.com/adfs`)。

AD FS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **AD FS** \> **管理者**に移動してエラーを確認します。

### <a name="fiddler"></a>Fiddler

追加のデバッグには Fiddler を使用することができます。 Fiddler について詳しい情報は、 [AD FS 2.0: Fiddler Web デバッガーを使って WS フェデレーション パッシブ サインインを分析する方法](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx) と [別の AD FS クレーム プロバイダーからの AD FS トークンのクラッキング](https://blogs.technet.microsoft.com/tangent_thoughts/2014/06/04/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider/) をご覧ください。

以下のセクションでは、 Microsoft Dynamics に返される要求に対する重点的なデバッグの手順を示します。

#### <a name="repocapture"></a>リポジトリ/キャプチャ

1. Fiddler を起動し、 **ツール \> オプション \> HTTPS** から **HTTPS トラフィックの復号化** を選択します。
2. トラフィックのキャプチャを開始します (ショートカット キーは F12 キーです)。 ツールの左下を確認すると、該当のトラフィックがキャプチャされていることを確認できます。
3. Internet Explorer の InPrivate モード、またはChrome の Incognito モードを使用して開きます。
4. Finance and Operations を開きます (例 `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`).
5. USERINFO.NETWORKALIAS のアカウントとパスワードを使用してログオンします。
6. ログイン後、Fiddler によるトラフィックのキャプチャを停止してください。

#### <a name="analyze"></a>分析

Fiddler の右側のウィンドウには、リクエストとレスポンスが上段と下段にに分割されていることを留意してください。 リクエストとレスポンスとでそれぞれ別個のフレームを取得するようなネットワーク トレースとは異なり、Fiddler はリクエストとレスポンスの両方を1 つのフレームで提供します。

1. Fiddlerを起動し、画面右上隅の **Inspectors** \> **Raw** を選択します。
2. 右下隅の **Cookie** を選択します。
3. **MSISAuth** を検索します。
4. AD FS をホストするには、結果が **200** 件ある行を選択します。
5. 上記で選択した上の行のなかで、 **302** 件の結果がある行を探します。 確認した行を選択します。

    AD FS URL、ホスト、ユーザー名、およびパスワードが表示されます。 

    > [!IMPORTANT]
    > プライバシー保護のため、状況に応じて個人を特定できる情報を削除してください。

    ![個人情報](media/Scrub-PII.png)

6. 次は、結果が **302** 件ある行を選択します。 URL が、 **.../namespaces/AXSF/** となっていることを確認します。
7. 上記で選択した行に示されているコード行を探してください。 

    ![コード行](media/Note-the-code.png)

8. 等号 (=) の後に表示されているコード値をコピーします。
9. <https://www.base64decode.org/> に移動し、上記でコピーしたコードを貼り付けます。
9. **Source charset** フィールドで、 **ASCII** を選択します。
10. **Decode** を選択します。
11. 表示された結果をコピーし、以下の手順に従います。

    - **upn** の値が、ユーザー名と一致していることを確認してください。
    - **unique_name** の値がテストで使用している Active Directoryユーザー名であることを確認してください。
    - **Active Directory ユーザーとコンピューター** \> **ドメイン** \> **ユーザー** に移動し、テスト中のユーザーが表示されることを確認します。

## <a name="sign-in-issues"></a>サインインの問題

サインインに関する問題が発生した場合には、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。 値が有効な場合は、プライマリ SQL Server マシンで次のコマンドを実行します。

```powershell
.\Reset-DatabaseUsers.ps1
```

タスク マネージャーの各 AOS マシンで、**AXService.exe** を選択し、**タスクの終了**を選択します。

ユーザーがリセットされたことを確認するには、AXDB SQL databaseで次の **select** 文を実行します。

```sql
select SID, NETWORKDOMAIN, NETWORKALIAS, * from AXDB.dbo.USERINFO where id = 'admin'
```

> [!NOTE]
> Azure Active Directory (Azure AD) 環境 (オンライン環境) では、SID はネットワーク エイリアスおよびネットワーク ドメインのハッシュの役割を果たします。 AD DS 環境 (オンプレミス環境) では、SID はネットワーク エイリアスのハッシュとして機能し、プロバイダーを識別します。

場合によっては、引き続きサインインができず、次のエラーが発生する可能性があります。

> 現在の資格情報でログインする権限がありません。 AD FS マシンで、サーバー マネージャー > ツール > AD FS の管理 に移動します。

このエラーが表示された場合は、次の手順に従ってください。

1. AD FS マシンで、 **Server Manager** \> **Tools** \> **AD FS Management** に移動します。
2. **AD FS** を右クリックし、**フェデレーション サービス プロパティの編集** を選択します。
3. **フェデレーション サービス 識別子** の値が、 **Userinfo.NetworkDomain** および **UserInfo.IdentityProvider** の値と一致していることを確認してください。
4. AD FS マシンで、Windows PowerShell を開き、 **Get-AdfsProperties** を実行します。
5. **IdTokenIssuer** の値が、手順3の **フェデレーション サービス 識別子** の値、および **Provisioning_AdminIdentityProvider** の値と一致していることを確認してください。 (これは **fabric:/AXSF Details** タブに表示されています。 **Service Fabric Explorer** \> **Cluster** \> **Applications** \> **AXSFType**)
3. Service Fabric Explorer で、 **Provisioning\_AdminPrincipalName** 値と **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。

上記の手順で問題が解決しない場合は、このトピックの 「 [AD FS](troubleshoot-on-prem.md#ad-fs) 」 を参照してください。

## <a name="systemdatasqlclientsqlexception-0x80131904-and-systemcomponentmodelwin32exception-0x80004005"></a>System.Data.SqlClient.SqlException (0x80131904) および System.ComponentModel.Win32Exception (0x80004005)

次のエラーのいずれかが表示される場合があります。

> System.Data.SqlClient.SqlException (0x80131904): 接続がサーバーで正常に確立されましたが、サインイン プロセス時にエラーが発生しました。 (プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは、信頼されていない機関によって発行されました。)

> System.ComponentModel.Win32Exception (0x80004005): 証明書チェーンは、信頼されていない機関によって発行されました

この場合、証明書がインストールされていないか、それらがしかるべきユーザーに結びついていません。 このエラーを解決するには、公開キー SQL サーバー証明書をすべての Service Fabric ノードに追加します。

## <a name="keyset-doesnt-exist"></a>Keyset が存在しません

キーセットが存在しないことが判明した場合は、スクリプトがすべてのコンピューターで実行されなていなかったことを意味します。 適切な設定の「VM の設定」セクション、および環境の配置トピックを確認し完了します。

- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#setupvms)
- [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupvms)

各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。

また、正しいドメインを使うことを検証する .csv ファイルを確認します。

## <a name="error-runasync-failed-due-to-an-unhandled-fabricexception-causing-replica-to-fault"></a>エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」

次のエラーが表示される場合があります。

> 未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException: 最初の Fabric アップグレードではコード バージョンと設定バージョンの両方を指定する必要があります。 要求された値: 0.0.0.0:

この場合、ClusterConfig.json ファイルで、 **diagnosticsStore** をネットワーク共有からローカル パスに変更します。 たとえば、**\\\\サーバー\\パス**を、規定値の **C:\\ProgramData\\SF\\DiagnosticsStore** に変更します。

## <a name="service-fabric-aos-node-error-during-build-the-execution-time-out-expired"></a>ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ

**エラー:**

> 操作を完了する前にタイムアウト期間が経過したか、サーバーが応答していません。  
> 明細書は終了しました。

一度に 1 つの AOS マシンのみ DB Sync を実行できます。 このエラーは無視しても問題ありません。 AOS VM のいずれかが DB Sync で実行されているため、他の VM が実行できないという警告が表示されたためです。 DB Sync が実行されていることを確認するには、イベント ビューアの、警告を生成していない AOS VM で**アプリケーションおよびサービスのログ** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize/Operational** の順に移動します。

## <a name="error-requirenonce-is-true-default-but-validationcontextnonce-is-null"></a>エラー、「RequireNonce が True (既定) ですが、validationContext.Nonce は Null です」

次のエラーが表示される場合があります。

> 「RequireNonce が True (既定) となっていますが、validationContext.Nonce は Null となっています」

このエラーは、クライアントにサインインした後も Internet Explorer で HTTP エラー 500 として表示されます。 Internet Explorer がセキュリティ強化の構成になっている場合、発行された nonce は検証できません。

クライアントにサインインするには、サーバー マネージャーを介して Internet Explorer のセキュリティ強化設定を無効にします。

## <a name="error-invalid-algorithm-specified--cryptography"></a>エラー、「無効なアルゴリズムが指定されている/暗号化」

"Invalid algorithm specified / Cryptography" エラーが発生した場合は、Microsoft Enhanced RSA および AES Cryptographic Provider を使用する必要があります。 詳細については、証明書の要件を参照してください。 また、credentials.json ファイルの構造が正しいことを確認します。

正しいプロバイダーを使用して証明書を再作成する必要がある場合は、次の手順に従います。

1. 正しいプロバイダーを使用して証明書を再度作成します。
2. **ConfigTemplate.xml** ファイルの変更。
3. クラスター内のすべてのコンピューターでインフラストラクチャ スクリプトを実行し、**Test-D365FOConfiguration.ps1** スクリプトに合格するかどうかを確認します。
4. LCS から環境を再構成します。

## <a name="an-unable-to-find-certificate-error-occurs-when-you-run-test-d365foconfigurationps1"></a>Test-D365FOConfiguration.ps1 を実行した際、「証明書を検出できません」エラーが発生

Test-D365FOConfiguration.ps1 を実行時に 「証明書を検出できません」 というエラーが発生した場合は、証明書または拇印がその他複数の用途で併用されているかどうかを確認します。 たとえば、クライアントと SessionAuthentication の証明書が併用されてされる場合、このエラーが発生します。 証明書を結合しないことをお勧めします。 詳細については、 証明書の必要要件を参照し、 **domain.com\\user** versus **domain\\user** 内 (たとえば、NETBIOS 構造) のacl.csv ファイルを確認してください。

## <a name="the-client-and-server-cant-communicate-because-they-dont-have-a-common-algorithm"></a>クライアントとサーバーは共通のアルゴリズムを持たないため通信できません

クライアントとサーバーが疎通できない場合は双方のアルゴリズムが異なることが原因です。作成した証明書が指定したプロバーダーを使用しているか確認をしてください。これについては"Plan and acquire your certificates" の項目で解説しています。ご利用の環境に応じた適切な設定と配置を行ってください。

- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#plancert)
- [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#plancert)

## <a name="find-a-list-of-group-managed-service-accounts"></a>グループ管理サービス アカウント の一覧の検索

すべてのグループとホストの一覧を検索するには、次のコマンドを実行します。

```
Get-ADServiceAccount -Identity svc-LocalAgent$ -Properties PrincipalsAllowedToRetrieveManagedPassword
```

## <a name="addcerttoserviceprincipal-script-fails-on-import-module"></a>Import-Module での AddCertToServicePrincipal スクリプトの失敗

**エラー:**

> Import-Module での AddCertToServicePrincipal スクリプトの失敗: ファイルまたはアセンブリ 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' またはその依存関係のうちのいずれか 1 つを読み込めませんでした。 厳密な名前の検証に失敗しました。 (HRESULT からの例外: 0x8013141A) には、同じモジュールの複数のバージョンがインストールされている場合があります。

**ステップ:** 問題を解決するには、次の手順に従います。

1. Windows PowerShell で次のコマンドを実行します。

    ```powershell
    Uninstall-Module -Name AzureRM
    Install-Module AzureRM
    ```

2. Windows PowerShell ウィンドウを閉じて、スクリプトを再度実行します。

## <a name="reportingservicessetupexe-error"></a>ReportingServicesSetup.exe エラー

**エラー:**

> ReportingServicesSetup.exe エラー: 0 : アプリケーション fabric:/ReportingService は10分後から OK ではありません。  
> アプリケーション: ReportingServicesBootstrapper.exe  
> フレームワーク バージョン: v4.0.30319  
> 説明: プロセスは未処理の例外によって中止されました。

**理由:** このエラーが発生した場合、厳密な名前検証はレポート サーバーで有効にされていますが、有効にしないでください。

**ステップ:** 問題を解決するには、レポート サーバー マシンで **config-PreReq** スクリプトを実行します。

## <a name="the-requested-operation-requires-elevation"></a>要求された操作には、昇格が必要です

AOS ユーザーはローカル管理者グループに属しておらず、ユーザー アカウント コントロール (UAC) が正しく無効化されていないために、この問題が発生します。 問題を解決するには、次の手順に従います。

1. 環境の適切な設定および配置トピックの「VMs とドメインを結合」のセクションで説明されているように、ローカル管理者として AOS ユーザーを追加します。

    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#joindomain)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#joindomain)

2. すべての AOS コンピューターで、**Config-PreReq** スクリプトを実行します。
3. **テスト構成**スクリプトがパスすることを確認します。
4. UAC が変更された場合は、変更を有効にする前にマシンを再起動する必要があります。

## <a name="files-in-use-errors"></a>使用中ファイルのエラー

「ファイルは使用中です」のエラーが発生した場合は、Service Fabric に示されている例外ルールを設定します。 詳細については、[環境設定](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)を参照してください。

## <a name="apply-deployable-packages-during-deployment"></a>配置中に配置可能パッケージを適用する

### <a name="package-deployment-fails-because-of-a-path-too-long-exception"></a>「パスが長過ぎる」例外によってパッケージの展開が失敗する

Microsoft Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。 文字数の制限を超過した場合、次のエラーが表示されます。

> System.IO.PathTooLongException: 指定されたパス、ファイル名、またはその両方が長すぎます。 完全に記述されたファイル名は 260 文字未満である必要があり、ディレクトリ名は 248 文字未満である必要があります。 at System.IO.PathHelper.GetFullPathName

この問題を回避するには、パッケージ名を短くし、パッケージをもう一度適用します。 または、オンプレミス資産の共有パス全体の長さを短くしてください。

### <a name="package-deployment-fails-because-of-a-serialization-error"></a>シリアル化エラーが原因でパッケージの展開に失敗する

パッケージ配置中、次のエラーが発生する場合があります。

> シリアル化バージョンの不一致が検出されたので、ランタイム DLL が配置されたメタデータと同期していることを確認してください。 「XXX」ファイルのバージョン DLL 「XXX」のバージョン

この場合は、パッケージが開発された環境のバージョンと、パッケージを配置する環境のバージョンが異なっている可能性があります。

この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。 パッケージのアップロード先にあるアセット ライブラリの**追加の詳細**セクションをクリックすることにより、パッケージ バージョンを確認することができます。 このエラーを修正するには、オンプレミス環境に配置されたバージョンと同じか、またはそれ以前のバージョンでパッケージを生成する必要があります。

### <a name="package-deployment-fails-because-of-dependencies-on-missing-modules"></a>欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する

依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次のようなメッセージが表示されます。

> パッケージ \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]
>
> パッケージ \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]
>
> パッケージ \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]

問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーで、**アプリケーションとサービス**を開き、**Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** の順で移動して、見つからないモジュールのあるイベントを表示します。 たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor です。

この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。 依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。 モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除できます。 詳細については、「[モデルのエクスポートとインポート](../dev-tools/models-export-import.md)」を参照してください。

### <a name="package-deployment-works-in-a-one-box-environment-but-not-in-the-sandbox-environment"></a>パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない

1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、一方ではサンドボックス環境には実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。 開発環境で作成されたパッケージが、サンドボックス環境ではなく、ワン ボックス環境にあるモジュールに依存する場合、パッケージはサンドボックス環境では動作しません。

この問題を解決するには、依存関係のあるすべてのモジュールを確認し、実稼動環境で不要なアダプターまたはその他のモジュールを使用しないようにしてください。 ビルド ボックスからパッケージを取得することをお勧めします。

## <a name="an-error-occurs-when-you-sign-in-to-on-premises-environments"></a>オンプレミス環境へのログイン時にエラーが発生

- **プラットフォーム更新 12:** **システム管理** \> **設定** \> **クライアント パフォーマンス オプション**に移動して、Skype 統合を無効にしてください。 アプリに移動するとき、`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true` の例のように、**?debug=true** を URL に追加します。
- **プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11:** 確認されている問題は、 Skype の アプリケーション プログラミング インターフェイス (API) が、オンプレミス環境へのサインインする機能に影響を及ぼしているというものです。 Microsoftはこの問題の解決方法を調査しています。 この問題を回避するために、次の例のように URL の末尾に **?debug=true** を追加できます。`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`

## <a name="the-local-agent-stops-working-after-the-tenant-for-the-project-from-lcs-is-changed"></a>ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します

更新されたテナントでローカル エージェントを構成するには、次の手順を実行します。

1. ローカル エージェントをアンインストールします。

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. ユーザーの環境での適切なセットアップと配置トピックの「テナントの LCS 接続のコンフィギュレーション」セクションにある手順を実行します。

    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#configurelcs)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

3. 新しいテナントに新しい LCS コネクタを作成します。
4. **local-agent.config** ファイルをダウンロードします。
5. ローカル エージェントをインストールします。

    ```powershell
    .\LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

## <a name="additional-deployments-for-example-two-sandbox-deployments-or-a-sandbox-and-production-deployment"></a>追加の配置 (たとえば、2 つのサンド ボックス展開、またはサンド ボックスおよび生産の配置)

追加の環境を展開すると、次のエラーが表示されます。

> \\Publish-ADFSApplicationGroup.ps1 -HostUrl `https://ax.d365ffo.onprem.contoso.com` New-AdfsApplicationGroup : MSIS9908: アプリケーション グループ ID は、AD FS コンフィギュレーションで一意である必要があります。

配備手順の次のセクションをスキップまたは変更することができます。

### <a name="plan-and-acquire-your-certificates-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdplancert-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdplancert"></a>証明書の計画と取得 ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#plancert) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#plancert) で記載されたものとして)

- 同一のオンプレミスのローカル エージェント証明書を使用する必要があります。
- 同一のスター証明書を使用することができます(AOS SSL および Service Fabric)。
- 残りの証明書は既存の環境の証明書とは異なる可能性があります。

### <a name="download-setup-scripts-from-lcs-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mddownloadscripts-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mddownloadscripts"></a>LCS からのセットアップ スクリプトのダウンロード ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#downloadscripts) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#downloadscripts) で記載されたものとして)

- ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。

### <a name="set-up-a-standalone-service-fabric-cluster-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdsetupsfcluster-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdsetupsfcluster"></a>([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#setupsfcluster) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster) に記載されているように) スタンドアロン Service Fabric クラスタを設定します

- ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。

### <a name="configure-lcs-connectivity-for-the-tenant-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdconfigurelcs-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdconfigurelcs"></a>テナント用 LCS 接続 のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configurelcs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs) で記載されたものとして)

- テナントに対して、このタスクを 1 回のみ実行する必要があります。

### <a name="configure-ad-fs-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdconfigureadfs-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdconfigureadfs"></a>AD FS のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configureadfs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configureadfs) で記載されたものとして)

- すでに完了しているので、スクリプト 1、スクリプト 2、スクリプト 3 はスキップできます。
- 新しい **hosturl** 値を使用している場合でも、.\\Publish-ADFSApplicationGroup.ps1 スクリプトは失敗します。 したがって、この手順を手動で完了する必要があります。

    1. AD FS マネージャーで、**AD FS** \> **アプリケーション グループ**に移動し、**Microsoft Dynamics 365 for Operations オンプレミス**を開きます。
    2. **Microsoft Dynamics 365 for Operations  オンプレミス - ネイティブ アプリケーション** を開きます。 新しい環境 (DNS) の リダイレクト URI を追加します。
    3. **Microsoft Dynamics 365 for Operations オンプレミス - 財務諸表 - ネイティブ アプリケーション** を開きます。 新しい環境 (DNS) の リダイレクト URI を追加します。
    4. **Microsoft Dynamics 365 for Operations オンプレミス - Web AP I** を開きます。 新しい環境 (DNS) のリダイレクト URI の 2 つのエントリを追加します。
    5. **Microsoft Dynamics 365 for Operations オンプレミス - 財務諸表 Web API** を開きます。 新しい環境 (DNS) の リダイレクト URI を追加します。

## <a name="redeploy-ssrs-reports"></a>SSRS レポートを再配置する

SF.SyncLog のエントリを削除して、AOS マシンの 1 つを再起動します。 AOS コンピューターは DB 同期を再実行し、レポートを配置します。

## <a name="add-axdbadmin-to-tempdb-after-a-sql-server-restart-via-a-stored-procedure"></a>ストアド プロシージャ経由で SQL Server を再起動した後、tempdb に axdbadmin を追加します。

SQL Server を再起動すると、tempdb データベースが再作成されます。 結果として、アクセス許可が不十分です。 マスター データベースでストアド プロシージャを作成する次のスクリプトを実行します。

```
\-----
USE [master]
GO
CREATE procedure [dbo].[CREATETEMPDBPERMISSIONS] as begin exec ('USE tempdb; declare @dbaccesscount int; select @dbaccesscount = COUNT(*) from master..syslogins where name = ''axdbadmin''; if (@dbaccesscount <> 0) exec sp_grantdbaccess ''axdbadmin''; ALTER USER [axdbadmin] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''axdbadmin''; EXEC sp_addrolemember N''db_datawriter'', N''axdbadmin''; EXEC sp_addrolemember N''db_ddladmin'', N''axdbadmin''; exec sp_grantdbaccess ''contoso\svc-AXSF$''; ALTER USER [contoso\svc-AXSF$] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_datawriter'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_ddladmin'', N''contoso\svc-AXSF$'';') end
GO
EXEC sp_procoption N'[dbo].[CREATETEMPDBPERMISSIONS]', 'startup', '1'
\-----
```

## <a name="error-updates-to-existing-credential-with-keyid-key-is-not-allowed"></a>エラー、「KeyId『\<key\>』による既存の資格情報の更新は許可されていません」

次のエラーが表示される場合があります。

> KeyId「\<key\>」を保持している既存の資格情報を更新することはできません。

この問題を解決するための手順は、オンプレミス プロジェクトのみをご利用しているか、オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用しているかによって異なります。

### <a name="if-have-only-an-on-premises-project"></a>場合設置プロジェクトのみ

オンプレミス プロジェクトのみの場合は、KeyId '\<key\>' を保持している既存の資格情報を更新することはできません。

> New-AzureRmADSpCredential : KeyId '\<key\>' による既存の資格情報の更新は許可されていません。  
> At C:\\InfrastructureScripts\\Add-CertToServicePrincipal.ps1:62 char:1  
> New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...  
> CategoryInfo : InvalidOperation: (:) \[New-AzureRmADSpCredential\], Exception  
> FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand

この問題を解決するには、次の PowerShell コマンドを実行します。

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName "00000015-0000-0000-c000-000000000000" -KeyId <key>
```

### <a name="if-you-have-both-an-online-project-and-an-on-premises-project"></a>オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合

オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合は、次の手順に従ってください。

1. Microsoft .NET フレームワーク version 4.7.2 がインストールされていることを確認します。
2. 以下のWindows PowerShell スクリプトを実行し、Azure PowerShell moduleをインストールします。

    ```powershell
    Install-Module -Name Az
    ```

3. 以下のWindows PowerShellスクリプトを実行し、新規証明書をアップロードします。

    ```powershell
    Import-Module -Name Az.Accounts
    Import-Module -Name Az.Resources

    Connect-AzAccount

    $servicePrincipalName = "00000015-0000-0000-c000-000000000000";
    $CertificateThumbprint = <Thumbprint of Agent Certificate>
    $cert = Get-ChildItem -path Cert:\CurrentUser\my | Where-Object { $_.Thumbprint -eq $CertificateThumbprint }
    if (!$cert)
    {
        $cert = Get-ChildItem -path Cert:\LocalMachine\my | Where-Object { $_.Thumbprint -eq $CertificateThumbprint }
        if (!$cert)
        {
            throw "Unable to find the certificate in the Local machine or Current User store"
        }
    }

    $keyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
    $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName $servicePrincipalName
    if (!$servicePrincipal)
    {
        throw "Unable to find the service principal"
    }
    New-AzADSpCredential -ObjectId $servicePrincipal.Id -CertValue $keyValue -EndDate $cert.NotAfter -StartDate $cert.NotBefore
    Get-AzADSpCredential -ObjectId $servicePrincipal.Id
    ```

4. 複数の証明書が存在する場合は、以下のコマンドを実行して重複する証明書を削除します。

    ```powershell
    Remove-AzADSpCredential -ServicePrincipalName "00000015-0000-0000-c000-000000000000" -KeyId <key>
    ```

## <a name="odbc-driver-17-is-required-for-platform-updates"></a>プラットフォームの更新には ODBC ドライバー 17 が必要です

プラットフォーム バイナリを最新に更新するには、Open Database Connectivity ODBC ドライバー 17 を使用します。 このアップグレードでは、古いバージョンの ODBC ドライバーに関連する安定性の問題を修正します。 [追加の設定](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites) に関するドキュメントが更新されており、次の変更が記載されています。各AOSサーバーにはODBC ドライバー 17 がインストールされている必要があります。 ODBC ドライバー 17 をインストールしない場合は、環境のメンテナンス処理中に DB 同期エラーが表示されます。

エラーの例を次に示します。

- Service Fabric で:

    > 問題のあるイベント: SourceId=「System.RA」、プロパティ =「ReplicaOpenStatus」、HealthState=「警告」、ConsiderWarningAsError=false。  
    > レプリカで、AOS3 で開いているときに複数の障害が発生しました。 API 呼び出し: IStatelessServiceInstance.Open(); Error = System.Exception (-2146233088)  
    > **DB の同期に失敗しました。**

- AOS コンピューターで:

    - イベント ビューアー \> カスタム ビュー \> 管理イベント:

        > アプリケーション: Microsoft.Dynamics.AX.Deployment.Setup.exe フレームワーク バージョン: v4.0.30319 説明: プロセスは未処理の例外によって中止されました。 例外情報: System.IO.FileNotFoundException at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(System.String\[\])

    - C:\\ProgramData\\SF\\AOSx\\Fabric\\work\\Applications\\AXSFType\_Appxx\\log:

        > Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -metadatadir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -sqluser "axdbadmin" -sqlserver "SQL-LS.contoso.com" -sqldatabase "AXDB" -setupmode servicesync -syncmode fullall -onprem
        >
        > ハンドルされない例外: System.IO.FileNotFoundException: **ファイルまたはアセンブリ 'aoskernel.dll'、あるいはその依存関係のうちのいずれか 1 つを読み込めませんでした。指定されたモジュールが見つかりませんでした。**
        > Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(String\[\] args) にて
        > 
        > **DB の同期に失敗しました。**

## <a name="a-no-subscription-found-in-the-context-error-occurs-when-you-run-add-certtoserviceprincipal"></a>Add-CertToServicePrincipal を実行すると、"コンテキストにサブスクリプションが見つかりません" エラーが発生します

最新バージョンの Windows PowerShell が原因で "コンテキストにサブスクリプションが見つかりません" エラーが発生することがあります。 この問題を解決するには、Windows PowerShellのバージョン5.7.0などの古いバージョンをインストールし、上書きしてください。

```powershell
# Install version 5.7.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 5.7.0

# Load version 5.7.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 5.7.0
```
## <a name="service-fabric-explorer-warnings-occur-after-you-restart-a-machine"></a>コンピューターの再起動後に Service Fabric Explorer の警告メッセージが表示される

**エラー:**

> エラー: event: SourceId='MonitoringAgentService', Property='ServiceState'.  
> System.Management.Automation.RuntimeException: エラー: **渡された GUID は WMI データ プロバイダーにより有効と認識されませんでした。** (HRESULT からの例外: 0x80071068)。 スタック トレース:

**手順:** この問題を解決するには、警告メッセージの原因であるアプリケーション パッケージを再起動します。 詳しくは、 [アプリケーション(AOS など)を再起動してください](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/troubleshoot-on-prem#restart-applications-such-as-aos) をご覧ください。

## <a name="the-internal-time-zone-version-number-that-is-stored-in-the-database-is-higher-than-the-version-that-is-supported-by-the-kernel-1312"></a>データベースに格納されている内部タイム ゾーンのバージョン番号が、カーネル (13/12) でサポートされているバージョンよりも大きくなっています。

このデータベースの同期エラーにより、新しいビルド (プラットフォーム更新 15) があったデータベースの上に古いプラットフォーム ビルド (プラットフォーム更新 12) が配置されてしまう可能性があります。

この問題を解決するには、 **SYSTIMEZONESVERSION** の値が重要になります。

```
select * from SQLSYSTEMVARIABLES where parm = 'SYSTIMEZONESVERSION'
```

エラー メッセージにて表示されたバージョンの値で [value] を更新します

```
update SQLSYSTEMVARIABLES set VALUE = 12 where parm = 'SYSTIMEZONESVERSION'
```

## <a name="printing-randomly-stops"></a>印刷がランダムに停止する

AOS サーバーにインストールされているすべてのネットワーク プリンターが、AXService.EXE プロセスが実行されている Windows サービス アカウントとして実行されていることを確認してください。

## <a name="ax-databasesynchronize-isnt-populated-with-events"></a>Ax-DatabaseSynchronize にイベントが設定されていません

プラットフォームの更新 20 およびそれ以降では、データベース同期ログに問題があり、イベント ビューアーで同期ログが **Ax-DatabaseSynchronize** の下に作成されません。

この問題を解決するには、 \<SF-dir\>\\AOS\_\<x\>\\Fabric\\work\\Applications\\AXSFType\_App\<X\>\\log に移動してください。 例えば次の場所に移動します。 C:\\ProgramData\\SF\\AOS\_11\\Fabric\\work\\Applications\\AXSFType\_App183\\log ここでは、DatabaseSynchronize からの出力された内容を確認できます。 Code\_AXSF\_M\_\<X\>.out files. このコンポーネントに関する問題をトラブルシューティングします。

## <a name="you-cant-access-finance-and-operations-aadsts50058-a-silent-sign-in-request-was-sent-but-no-user-is-signed-in"></a>Finance and Operations にアクセスできません: 「AADSTS50058: サイレント サインインの要求が送信されましたが、ログインしているユーザーがいません」

Finance and Operations へのログイン資格情報を入力すると、ブラウザでアプリケーションのレイアウトが少しの間表示されます。 しかしその後、Finance and Operations外部へのリダイレクトを試みた結果、次のエラーが出て失敗します。

> AADSTS50058: サイレント サインイン要求が送信されましたが、ユーザーがログインしていません。

ユーザーのセッションを表すために使用する Cookie が Azure AD への要求で送信されませんでした。 これは、 Internet Explorer または Microsoft Edge を使用している場合で、webアプリケーションが送信しているサイレント サインインのリクエストが Azure AD エンドポイント (login.microsoftonline.com)とは異なる IEのセキュリティ ゾーンに設定されている場合に発生する可能性があります。

この問題を解決するには、次の PowerShell コマンドを実行します。

この問題を解決するには、次の SQL Server query を実行します。

```
update [AXDB].[dbo].[SYSCLIENTPERF] set SkypeEnabled = 0
```

または、**クライアント パフォーマンス オプション** ページの **Skype プレゼンスが有効** オプションを無効にします (**システム管理** \> **設定** \> **クライアント パフォーマンス オプション**)。 この方法を使用するには、Finance and Operations にログインできる必要があります。 そのため、最初にブラウザのリダイレクトをブロックする必要があります。 Skypeのプレゼンス機能を無効にすると、リダイレクトのブロックを解除しても構いません。

Chrome ブラウザーでは、最初からリダイレクトがブロックされています。

## <a name="error-there-was-an-error-during-codepackage-activation-service-host-failed-to-activate-error0x8007052e"></a>エラー: CodePackage の有効化でエラーが発生しました。 サービス ホストの有効化に失敗しました。 エラー: 0x8007052e"

新規インストールの際に以下のエラーが発生する可能性があります。

> エラー イベント: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'。 CodePackage の有効化でエラーが発生しました。サービス ホストの有効化に失敗しました。 エラー: 0x8007052e

このエラーと同じエラーが、AXSFサービスでも発生します。

この問題を解決するには、次の手順に従います。

1. [エージェント共有パス](setup-deploy-on-premises-pu12.md#setupfile) にて、 **netstandard.dll** ファイルを見つけます。 このファイルは、例えば \\wp\\\<名\>\\StandaloneSetup -\<バージョン\>\\アプリケーション\\AOS\\AXServiceApp\\AXSF\\コード\\在庫置場\\netstandard.dll に多くの場合存在します。
2. それぞれの AOS サーバーにて、管理者権限で コマンド プロンプトを開き、次のコマンドを実行します。

    ```
    "C:\Program Files (x86)\Microsoft SDKs\Windows\v8.1A\bin\NETFX 4.5.1 Tools\gacutil.exe" -i <path from step 1.>\netstandard.dll /f
    ```

3. Service Fabric から **AXBootstrapperApp** を削除します。

    1. **fabric:/Bootstrapper/AXBootstrapper** サービス を削除します。
    2. **fabric:/Bootstrapper** アプリケーションを削除します。
    3. **AXBootstrapperAppType** のプロヴィジョニングを解除します。

4.  LCS から環境を再配置します。

## <a name="sql-server-2016-service-pack-2-is-recommended-for-reporting-services-instances"></a>Reporting Servicesのインスタンス には SQL Server 2016 service pack 2 を推奨します。

LCSにてサービス操作を行うと次のエラーが表示されることがあります:

> プロセスが次のファイルにアクセスできません ' c:\\Program Files\\Microsoft SQL Server\\MSRS13.MSSQLSERVER\\Reporting Services\\ReportServer\\bin\\Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll' 別のプロセスによって使用されています。

この問題は Reporting Services が Microsoft Dynamics .dllファイル をロックしているために発生します。 Reporting Servicesのインスタンスには、SQL Server 2016 service pack 2をインストールすることを推奨しています。

> [!NOTE]
> サービス パック2のインストールが必要し、累積的な更新を追加または修正プログラムをインストールする必要がないです。
