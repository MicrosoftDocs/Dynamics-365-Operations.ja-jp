---
title: オンプレミス配置のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (on-premises) の展開のトラブルシューティング情報を提供します。
author: PeterRFriis
ms.date: 04/05/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: d04522c972ed41d8c13a6db9fb83d0b69ce02784
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565708"
---
# <a name="troubleshoot-on-premises-deployments"></a>オンプレミス配置のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance + Operations (on-premises) の展開のトラブルシューティング情報を提供します。

## <a name="access-service-fabric-explorer"></a>Service Fabric Explorer へのアクセス

Service Fabric Explorer には、Web ブラウザーと既定のアドレス `https://sf.d365ffo.onprem.contoso.com:19080` を使ってアクセスできます。

アドレスを確認するには、環境の適切なセットアップおよび配置トピックの「DNS ゾーンの作成と A レコードの追加」セクションで使用されていた値をメモします。

- [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#createdns)
- [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#createdns)

クライアント証明書が、サイトにアクセスするマシンの証明書、cert:\\CurrentUser\\My に含まれている場合のみ、サイトにアクセスできます (証明書マネージャーで、**証明書 - 現在のユーザー** \> **個人** \> **証明書** に移動します。) サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。

## <a name="monitor-the-deployment"></a>配置の監視

### <a name="identify-the-primary-orchestrator"></a>プライマリ オーケストレータを識別します。

Service Fabric Explorer でローカル エージェントなどのステートフル サービスのプライマリ インスタンスとなっているマシンを判別するには、**クラスター** \> **アプリケーション** \> **\<*intended application example*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** を展開します。

プライマリ ノードが表示されます。 ステートレス サービスまたは残りのアプリケーションについては、すべてのノードを確認する必要があります。

次のポイントに注意します。

- OrchestrationService は、Finance + Operations の配置およびサービス アクションを調整します。
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

    ![カスタム表示を作成します。](media/Create-Custom-View.png)

2. **イベント ログ** フィールドで **Dynamics** を選択します。

    ![Dynamics を選択します。](media/Select-Dynamics.png)

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

Service Fabric アプリケーションのさらなる詳細については、 C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log のログファイルを参照してください。

### <a name="lifecycle-services"></a>Lifecycle Services

Microsoft Dynamics Lifecycle Services (LCS) で環境のに対する現在の配置ステータスに注意してください。

## <a name="a-time-out-error-occurs-when-a-service-fabric-cluster-is-created"></a>Service Fabric cluster の作成時にタイムアウト エラーが発生する

該当するセットアップ トピックの "スタンドアロン Service Fabric Cluster のセットアップ" セクションおよび環境の配置トピックに記載されているように Test-D365FOConfiguration.ps1 を実行します。 エラーに注意してください。

- [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#setupsfcluster)
- [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#setupsfcluster)


これらの手順を必ず実行してください。

- すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。
- Service Fabric Server 証明書にすべての Service Fabric ノード上にネットワーク サービス用アクセス制御リスト (ACL) が含まれていることを確認します。
- [環境設定](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) で記載されているウイルス対策の除外を確認します。

## <a name="a-time-out-error-occurs-while-youre-waiting-for-installer-service-to-be-completed-for-machine-xxxx"></a>インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウト エラーが発生する

インターネット プロトコル (IP) アドレスごとに (つまり、コンピューターごとに) 1 つのノード タイプがサポートされます。 ノードが同じマシン上で再利用されているかどうかを確認してください。 たとえば、AOS および ORCH は、同一のマシン上に存在してはならず、ConfigTemplate.xml が正しく定義されている必要があります。

## <a name="remove-a-specific-application"></a>特定のアプリケーションを削除

配置の削除またはクリーンアップに LCS を使用することをお勧めします。 ただし、必要に応じて、アプリケーションを削除する Service Fabric Explorer を使用することもできます。

Service Fabric エクスプローラーで、**アプリケーション ノード** \> **アプリケーション** \> **MonitoringAgentAppType-Agent** に移動します。 **ファブリック:/エージェント監視** の横にある省略記号ボタン (**...**) を選択し、アプリケーションを削除します。 アプリケーションの完全な名前を入力して、アプリケーションの削除を確認します。

また、省略記号ボタンの選択および **非引当タイプ** の順に選択することにより、MonitoringAgentAppType-Agent を削除することができます。 アプリケーションの削除を確認するために、正式名称を入力します。

## <a name="remove-all-applications-from-service-fabric"></a>Service Fabric からすべてのアプリケーションを削除

次のスクリプトは、LocalAgent および LocalAgent の監視エージェントを除く、すべての Service Fabric アプリケーションを削除してプロビジョニング解除します。 オーケストレータ仮想マシン (VM) 上でこのスクリプトを実行する必要があります。

```powershell
$applicationNamesToIgnore = @('fabric:/LocalAgent', 'fabric:/Agent-Monitoring', 'fabric:/Agent-LBDTelemetry')
$applicationTypeNamesToIgnore = @('MonitoringAgentAppType-Agent', 'LocalAgentType', 'LBDTelemetryType-Agent')

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

2. エラーが発生した場合は、**CleanFabric.ps1** コマンドを使用して、クラスタ内の特定のノードを削除します。 このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。
3. 既定の場所を使用している場合、**C:\\ProgramData\\SF** フォルダーを削除します。 それ以外の場合、指定したフォルダーを削除します。

    "アクセス拒否" エラーが発生した場合は、Microsoft Windows PowerShell を再起動するか、マシンを再起動します。

## <a name="clean-up-an-existing-environment-and-redeploy"></a>既存環境のクリーンアップと再配置

既存の環境をクリーンアップして再配置するには、以下の手順を実行します。

1. LCS でプロジェクトを開き、**環境** セクションで展開を削除します。

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

    - [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md)
    - [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md)
  

5. LCS でプロジェクトを開き、必要に応じて LCS のオンプレミス コネクタを更新します。

    1. 環境の LCS オンプレミス コネクタを再作成するか、または既存のコネクタの設定を編集します。

        LCS の値を簡単にコピーするには、.\\Get-AgentConfiguration.ps1 script を使用します。

    2. 最新のローカル エージェント コンフィギュレーション、localagent config.json をダウンロードします。

6. 環境に適したセットアップと展開のトピックで次の指示に従って、再度展開します。

    - [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md)
    - [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md)

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

### <a name="issue"></a>問題点

**エラー :** ローカル エージェントをインストールすると、次のエラーが表示されます。

```stacktrace
LocalAgentCLI.exe Error: 0 : Exception System.InvalidOperationException: unable to get settings for telemetry setup component
    at LBDTelemetryCommon.LBDTelemetrySetupManager.GetComponentSettings()
    at LBDTelemetryCommon.LBDTelemetrySetupManager.ApplyParameters()
    at LocalAgentCLI.Program.Main(String[] args)
Press any key to exit
```

**理由:** ローカル エージェント バージョン 2.3.0 またはそれ以降のバージョンをインストールしようとしていますが、使用している localagent-config.json ファイルが最新ではありません。

**手順:** [オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector) の 「コネクタ構成とオンプレミスのローカル エージェントのインストール」 セクションの手順に従って、localagent-config.json ファイルの新しいバージョンを LCS から入手します。

localagent-configjson ファイルの **コンポーネント** セクションで次の値を手動で追加することもできます。
```json
{
    "name": "LBDTelemetry",
    "placementCriteria": "(IsOrchestratorEnabled == True)",
    "parameters": {
        "applicationPackagePath": {
            "value": "Applications\\LBDTelemetry"
        }
    }
},
```

### <a name="issue"></a>問題点

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

    - [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#configurelcs)
    - [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#configurelcs)

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

    - [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#setupfile)
    - [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#setupfile)

4. ローカル エージェントをアンインストールします。
5. ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。
6. 新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。

### <a name="error"></a>エラー

**エラー:** サービス操作を行うと次のエラーが表示されます:

> コマンドの抽出セットアップ フォルダーを取得できません

**理由:** そのファイル共有は削除または変更されました。

**手順:** ファイル共有の設定内容を確認するには、Microsoft SQL Server Management Studio を開いてオーケストレータ データベースで次のクエリを実行します:

```sql
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

[データベースを構成する](setup-deploy-on-premises-pu12.md#configuredb) プロシージャを実行するときに SQL Server インスタンスが名前付きインスタンスの場合は、**-DatabaseServer \[FQDN/Instancename\]** パラメーターを使用します。

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
    > これらのスクリプトは、**常時オン** に設定されているときは機能しません。 データベースは最初にプライマリ ノードに作成されてから複製される必要があります。

### <a name="error"></a>エラー

**エラー:**

> RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。 ---\> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'

**理由:** ローカル エージェント マシンは lcsapi.lcs.dynamics.com に接続できません。 「リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'」に対する AX-BridgeService イベント ログを確認します。

**ステップ:** エラーを解決するには、次の手順に従います。

1. **psping lcsapi.lcs.dynamics.com:80** を実行します。
2. 前述のコマンドから応答を受信しない場合は、組織の IT 部門に問い合わせます。 ファイアウォールが lcsapi へのアクセスをブロックしているか、もしくはプロキシの問題が発生しています。

    ```Console
    lcsapi.lcs.dynamics.com:443
    login.windows.net:443
    uswelcs1lcm.queue.core.windows.net:443
    www.office.com:443
    login.microsoftonline.com:443
    dc.services.visualstudio.com:443
    uswelcs1lcm.blob.core.windows.net:443
    uswedpl1catalog.blob.core.windows.net:443
    ```

## <a name="infrastructure-scripts-errors"></a>インフラストラクチャ スクリプト エラー

### <a name="issue"></a>出庫

**エラー:** Test-D365FOConfiguration.ps1 or Test-D365FOConfiguration-AllVMs.ps1 を実行すると、メッセージを受信します:

```stacktrace
"Get-LocalGroupMember : Failed to compare two elements in the array.
At C:\Infrastructure\Scripts\Test-D365FOConfiguration.ps1:79 char:9
+         Get-LocalGroupMember -Group 'Administrators' | `
+         ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Get-LocalGroupMember], InvalidOperationException
    + FullyQualifiedErrorId : An unspecified error occurred.,Microsoft.PowerShell.Commands.GetLocalGroupMemberCommand" 
```

**理由:** PowerShell コマンドレット Get-LocalGroupMember にバグがあり、無効なエントリがあると失敗します。

**ステップ:** スクリプトが失敗しているマシンで、**ローカル ユーザーとグループ** を開きます。 管理者グループに移動し、次の画像で強調表示されているようなエントリを持つエントリをすべて削除します。

![無効な SID。](media/InvalidSID.png)

このエラーを受け取ったすべてのマシンでこれを実行します。 変更が完了したら、スクリプトを再実行してください。

## <a name="restart-applications-such-as-aos"></a><a name="restartapplications"></a>アプリケーション (AOS など) を再起動

Service Fabric で、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード** の順に展開します。 省略記号ボタン (**...**) を選択し、**再起動** を選択します。 求められたらコードを入力します。

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
    > **-UpgradeReplicaSetCheckTimeout** は SSRS と Management Reporter の PreUpgradeSafetyCheck をスキップするために使用します。 詳細については、[Service Fabric サービスのアップグレードが動作しない](https://github.com/Azure/service-fabric-issues/issues/595) を参照してください。 **UpgradeDomainTimeoutSec 600 UpgradeTimeoutSec 1800** を使用することもできます。 詳細については、[アプリケーション アップグレード パラメーター](/azure/service-fabric/service-fabric-application-upgrade-parameters) を参照してください。

    ```powershell
    Start-ServiceFabricClusterUpgrade -Code -CodePackageVersion 6.1.472.9494 -Monitored -FailureAction Rollback -UpgradeReplicaSetCheckTimeout 30
    ```

4. アップグレードの状態を取得します。

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

詳細については、[アプリケーション アップグレードのトラブルシューティング](/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)を参照してください。

新しい Service Fabric リリースの時期については、[Azure Service Fabric チームのブログ](https://blogs.msdn.microsoft.com/azureservicefabric/) を参照してください。

アップグレード後に Service Fabric Explorer で警告が表示された場合は、ノードを記録して、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード** を展開して再起動してください。 省略記号ボタン (**...**) を選択し、**再起動** を選択します。
 
## <a name="error-unable-to-load-dll-fabricclientdll"></a>エラー、「DLL 'FabricClient.dll' を読み込むことができません」

"DLL 'FabricClient.dll' をロードできません" というエラーが表示された場合は、Windows PowerShellを 閉じて再起動してください。 エラーが引き続き発生する場合は、コンピューターを再起動します。

## <a name="what-cluster-id-should-be-used-in-the-agent-configuration"></a>エージェント コンフィギュレーションでどのようなクラスター ID を使用する必要がありますか。

クラスタ ID は、任意のグローバル一意識別子 (GUID) です。 この GUID は、追跡目的で使用されます。

## <a name="encryption-errors"></a>暗号化エラー

暗号化エラーの例は "AXBootstrapperAppType"、"Bootstrapper"、"AXDiagnostics"、"RTGatewayAppType"、"ゲートウェイの潜在的なエラー関連"、 "Microsoft.D365.Gateways.ClusterGateway.exe" を含みます。

AOS アカウント パスワードを暗号化するために使用されたデータ暗号化証明書がマシンにインストールされていない場合、これらのエラーのいずれかが発生することがあります。 この証明書が証明書 (ローカル コンピューター) に含まれているか、プロバイダーの種類が正しくない可能性があります。

エラーを解決するには、credentials.json ファイルを検証します。 インフラストラクチャ フォルダーを AOS ノードにコピーします。またはインフラストラクチャ フォルダーがファイル共有に存在する場合は、AOS ノードからスクリプトを実行します。

1. 次のコマンドを (AOS1 上で) 実行することにより、テキストが正しく復号化されていることを確認します。

    ```powershell
    .\Configure-CredentialsJson.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -Action Decrypt
    ```

2. **Credentials.json** ファイルを開き、資格情報が正しいか確認します。
3. **Credentials.json** ファイルを再暗号化します。

    ```powershell
    .\Configure-CredentialsJson.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -Action Encrypt
    ```

4. いずれかの資格情報の更新が必要な場合は、サービス操作をトリガーする必要があります。 進行中のサービス操作が失敗した場合、[LCS](https://lcs.dynamics.com) から操作を再試行することで資格情報が更新されたことを確認できます。 環境が既に配置済みの状態である場合は、[LCS](https://lcs.dynamics.com) で、SQL Server を更新する環境の **完全な詳細** リンクを選択し、**管理** を選択してから、**更新の設定** を選択します。 設定は変更しないでください。 **準備** を選択し、準備が完了するまで待機してから、**環境の更新** を選択して環境の更新を開始します。

このエラーも、**''** パラメーターが ApplicationManifest ファイルで定義されていない場合にも発生させることができます。 このパラメータが定義されているどうかを確認するには、イベント ビューアーで、**カスタム ビュー** \> **管理イベント** に移動し、**Microsoft-Service Fabric** ソース カテゴリのエラーに注意します。

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

証明書 や ACL が見つからない、拇印の入力が間違っている場合は、特殊文字を確認し、C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt で拇印を検索してください。

次のコマンドを使用して暗号化されたテキストを検証することもできます。

```powershell
.\Configure-CredentialsJson.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -Action Decrypt
```

「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACLs を確認してください。

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
    .\Configure-CredentialsJson.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -Action Encrypt
    ```

7. いずれかの証明書を変更する必要がある場合、もしくは構成が正しくない場合は、次の手順を実行してください:

    1. **ConfigTemplate.xml** ファイルを編集して、正しい値が出るようにします。
    2. すべてのセットアップ スクリプトと **Test-D365FOConfiguration** スクリプトを実行します。

8. credentials.json ファイルが変更された場合、実行する必要のあるアクションは、LCS の環境ステータスによって異なります:

    - 環境が LCS に配置されている場合は、次の手順に従います:

        1. 環境ページに移動して、**管理** を選択します。
        1. **更新プログラムの設定** を選択します。
        1. 設定は変更しないでください。 **準備** を選択します。
        1. 数分後に、環境が準備され、**配置** を選択できます。

    - LCS で環境が失敗状態の場合は、**再試行** を選択します。 新しい Credentials.json ファイルは、再試行操作中に使用されます。

## <a name="gateway-fails-to-deploy"></a>ゲートウェイで配置に失敗する

**問題:** イベント ビューアー ログに次のエラーが表示されます。

```stacktrace
Message Module aos failed Detail System.InvalidOperationException: Gateway app and Bootstrapper app are not healthy at AOSSetupHybridCloud.Program.Main(String[] args) 
at System.AppDomain._nExecuteAssembly(RuntimeAssembly assembly, String[] args) 
at System.AppDomain.ExecuteAssembly(String assemblyFile, String[] args) 
at System.AppDomain.ExecuteAssembly(String assemblyFile, String[] args) 
at SetupCore.SetupManager.LaunchProcessInAppDomain(String startupExe, String workingDir, String currentFolder, String[] moduleArgs) 
at SetupCore.SetupManager.<>c__DisplayClass12_1.<InvokeModules>b__6()
```

ゲートウェイ アプリケーションの SFExplorer には、次のエラー メッセージも表示されます。

```stacktrace
'System.RA' reported Warning for property 'ReplicaOpenStatus'.
Replica had multiple failures during open on AOS_13. API call: IStatelessServiceInstance.Open(); Error = System.InvalidOperationException (-2146233079)
Category does not exist.
   at System.Diagnostics.PerformanceCounterLib.CounterExists(String machine, String category, String counter)
   at System.Diagnostics.PerformanceCounter.InitializeImpl()
   at System.Diagnostics.PerformanceCounter..ctor(String categoryName, String counterName, String instanceName, Boolean readOnly)
   at System.Diagnostics.PerformanceCounter..ctor(String categoryName, String counterName, String instanceName)
   at Microsoft.Dynamics.LBD.Gateways.ClusterGateway.Helpers.CpuPerfCounter..ctor()
   at Microsoft.Dynamics.LBD.Gateways.ClusterGateway.GzipContentDelegatingHandler..ctor()
   at Microsoft.Dynamics.LBD.Gateways.ClusterGateway.ClusterGateway.ConfigureApp(IAppBuilder appBuilder)
   at Microsoft.Owin.Hosting.Engine.HostingEngine.Start(StartContext context)
   at Microsoft.Dynamics.LBD.Gateways.Common.OwinCommunicationListener.b__9_0()
   at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.d__10`2.MoveNext()
```

**理由:** ゲートウェイで必要となるパフォーマンス カウンターへのポインターが破損している可能性があります。

**解決 :** ゲートウェイが正常でないすべての AOS ノードの、管理者として実行されているコマンド プロンプト ウインドウで **lodctr /R** を実行します。 パフォーマンス カウンターを再構築できないことを示すエラーメッセージが表示された場合は、コマンドを再度実行します。 

## <a name="management-reporter"></a>Management Reporter

プロバイダーを登録することで、追加のログを実行できます。 プロバイダーを登録するには、LCS 共有資産ライブラリで、資産タイプとして **モデル** を選択してから、**Microsoft Dynamics 365 Finance + Operations (on-premises)、LBDMRDeployerTroubleshooter** 資産をダウンロードします。 **プライマリ** オーケストレータ マシンにダウンロードされた ZIP ファイルをコピーし、解凍してから、次のコマンドを実行します。 (プライマリ インスタンスであるマシンを判別するには、Service Fabric Explorer で、**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** の順に展開します。)

> [!NOTE]
> イベント ビューアーの結果が正しく表示されない場合 (たとえば、単語が切り詰められた場合など)、最新のマニフェストおよび .dll ファイルを取得してください。 最新のマニフェストと .dll ファイルを取得するには、エージェント ファイル共有の WP フォルダに移動します。 この共有は、適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックで作成されました。
> 
> - [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#setupfile)
> - [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#setupfile)
> 
> **例:** \[*エージェント共有*\]\\wp\\\[*配置名*\]\\StandaloneSetup-...\\アプリ\\ ETWManifests

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"}
```

プロバイダーの登録を解除する必要がある場合は、次のコマンドを使用します。

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"} -Unregister
```

プロバイダーが登録されると、新しい配置についての追加詳細は **アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** でイベント ビューアーにログインされます。 次のフォルダが表示されます:

- MR-Logger
- MR-Sql

新しいフォルダーを表示するには、イベント ビューアーを終了して、再表示する必要があります。 追加の詳細を表示するには、もう一度環境を配置する必要があります。

###  <a name="could-not-load-file-or-assembly-entityframework"></a><a name="FREntityFramework"></a> ファイルまたはアセンブリ EntityFramework を読み込めませんでした

**問題**: ローカル エージェント バージョン 2.3.1 以降を実行していて、プラットフォーム更新プログラム 29 またはそれ以前を含むパッケージを展開しているときに、イベント ログで次の stacktrace を受け取りました。

```stacktrace
System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. --->
System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. --->
System.IO.FileNotFoundException: Could not load file or assembly 'EntityFramework, Version=6.0.0.0,
Culture=neutral, PublicKeyToken=b77a5c561934e089' or one of its dependencies. The system cannot find the file
specified. at Microsoft.Dynamics.Integration.Service.Utility.AdapterProvider.RefreshAdapters()
--- End of inner exception stack trace ---
 ```

**解決策**: TSG\_UpdateFRDeployerConfig.ps1 を使用します。 詳細については、[TSG_UpdateFRDeployerConfig.ps1](onprem-tsg-implementations.md#frdeployer)を参照してください。

### <a name="unable-to-deploy-financial-reporting-service"></a>財務報告サービスを配置できません

**問題:** 次のエラーが Service Fabric のアプリケーション ログにあるため、財務報告に対するプラットフォーム更新プログラム 26 以降の配置を完了できません。

```stacktrace
Application: FinancialReportingDeployer.exe Framework Version: v4.0.30319  
Description: The process was terminated due to an unhandled exception. 
Exception  Info: System.DllNotFoundException at  
Microsoft.Cloud.InstrumentationFramework.NativeIfxInterop.InitializeIfxFromCloudAgentConfigureSamplingAndTracing_x64(System.String,  System.String, UInt32, UInt32, Boolean) at  Microsoft.Cloud.InstrumentationFramework.IfxInitializer.IfxInitialize(System.String,  Microsoft.Cloud.InstrumentationFramework.InstrumentationSpecification,  Microsoft.Cloud.InstrumentationFramework.AuditSpecification) at  Microsoft.Dynamics.Performance.Logger.IfxLogger..cctor() Exception Info:  System.TypeInitializationException at  
Microsoft.Dynamics.Performance.Logger.IfxLogger..ctor(System.String,  Microsoft.Dynamics.Performance.Logger.IfxLoggerOptions) at  
Microsoft.Dynamics.Performance.Logger.IfxLoggerProvider.CreateLogger(System.String)  at  
Microsoft.Extensions.Logging.Logger..ctor(Microsoft.Extensions.Logging.LoggerFactory,  System.String) at  
```

**理由:** Visual Studio 2013 の Microsoft Visual C++ 再頒布可能パッケージが正しくインストールされていないか、MR ノードの一部またはすべてが破損しています。

**手順:** Visual Studio 2013 の Microsoft Visual C++ 再頒布可能パッケージのインストールを再実行します。

### <a name="an-error-occurs-while-addaxdatabasechangetracking-is-running"></a>AddAXDatabaseChangeTracking の実行中に発生するエラー

Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet) で AddAXDatabaseChangeTracking を実行しているときにエラーが発生した場合は、フル パスが正しいことを確認してください。 フル パスの例は **ax.d365ffo.onprem.contoso.com** です。

スター証明書での問題が原因でエラーが発生する可能性もあります。 たとえば、リモート証明書 CN=\*.d365ffo.onprem.contoso.com には、無効な、またはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。

### <a name="run-the-initialize-database-script-and-validate-that-databases-have-correct-users"></a>データベース初期化スクリプトを実行し、データベースのユーザーが適切であることを検証

AddAXDatabaseChangeTracking イベントのみを受け取った場合は、`https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService` にアクセスし、Finance + Operations の MetadataService サービスにアクセスしてみてください。

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

**手順:** URL を手動で開き、アドレスにアクセスできることを確認します。 詳細については、イベント ビューアーで "InnerException" のテキストが存在するかどうか確認してください。

### <a name="error-on-importdefaultreports"></a>ImportDefaultReports のエラー

配置中に Management Reporter レポートがチェックアウトされると、配置処理は失敗します。 レポートがチェック アウトされているかどうかを表示するには、FinancialReporting データベースで次の **選択** 明細書を実行します。

```sql
select checkedoutto, * from Reporting.ControlReport where checkedoutto is not null
select checkedoutto, * from Reporting.ControlRowMaster where checkedoutto is not null
select checkedoutto, * from Reporting.ControlColumnMaster where checkedoutto is not null
```

どのユーザーがオブジェクトをチェック アウトするかを知るには、次の **選択** ステートメントを実行します。

```sql
select * from Reporting.SecurityUser where UserID = ''
```

この問題を手動で解決するには、以下のテーブルを次のコマンドを使用して更新し、 **checkedoutto** を **null** に設定します。

```sql
update Reporting.ControlReport set checkedoutto = null where checkedoutto is not null
update Reporting.ControlRowMaster set checkedoutto = null where checkedoutto is not null
update Reporting.ControlColumnMaster set checkedoutto = null where checkedoutto is not null
```

## <a name="axdbadmin-cant-connect-to-the-database-server-sql-lscontosocom"></a>axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。

**理由:** AXDB データベースに接続するためのアクセス許可がありません。

**ステップ:**

1. 既に存在する場合は、データベースから axdbadmin ユーザーを削除します。
2. **ConfigTemplate.xml** ファイルで、**userName** 属性を更新することで、AXDB データベースに追加する必要があるユーザー名を指定します。

    ```xml
    <Security>
        <User refName="axdbadmin" type="SqlUser" userName="axdbadmin" />
    </Security>
    ```

3. [データベースの構成](./setup-deploy-on-premises-pu41.md#configuredb)の説明に従って、初期化データベース スクリプトを再実行して axdbadmin ユーザーを追加します。

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

**ADFS** \> **アプリケーション グループ** の順に移動して、AD FS マネージャーを確認します。 **Microsoft Dynamics 365 for Operations オンプレミス** をダブルクリックします。 その後、**ネイティブ アプリケーション** で、**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション** をダブルクリックします。

**リダイレクト URI** 値に注意してください。 Finance + Operations の DNS 前方参照ゾーンに一致させる必要があります。

### <a name="error-could-not-establish-trust-relationship-for-the-ssltls-secure-channel"></a>エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」

「SSL/TLS のセキュリティで保護されているチャネルに対する信頼関係を確立できませんでした」というエラーが表示された場合は、次の操作を行います。

1. Service Fabric で、**クラスタ** \> **アプリケーション** \> **AXSFType** \> **fabric:/AXSF** の順に移動し、**詳細** タブでスクロールし、**Aad\_AADMetadataLocationFormat** および **Aad\_FederationMetadataLocation** の URL に注意します。
2. AOS からそれらの URL を参照します。
3. 詳細については、AOS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** の順に移動します。
4. AD FS 証明書が信頼されていることを確認します。

    1. AD FS 証明書を確認します。 AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理** に移動します。
    2. **AD FS** \> **サービス** \> **証明書** を展開し、証明書を記録しておきます。 たとえば、1 つの証明書は、dc1.contoso.com の場合があります。
    3. AOS マシンの、Microsoft 管理コンソール証明書スナップインで、**証明書 (ローカル コンピューター)** \> **信頼済ルート証明機関** \> **証明書** の順に移動し、AD FS 証明書が一覧表示されていることを確認します。

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

AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理** \> **サービス** に移動します。 **フェデレーション サービス プロパティの保守と編集** を右クリックします。 **フェデレーション サービスの識別子** は **USERINFO.NETWORKDOMAIN** の値と一致している必要があり、URL に **https** が入っている必要があります (たとえば `https://DC1.contoso.com/adfs`)。

AD FS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **AD FS** \> **管理者** に移動してエラーを確認します。

### <a name="fiddler"></a>Fiddler

追加のデバッグには Fiddler を使用することができます。 Fiddler について詳しい情報は、 [AD FS 2.0: Fiddler Web デバッガーを使って WS フェデレーション パッシブ サインインを分析する方法](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx) と [別の AD FS クレーム プロバイダーからの AD FS トークンのクラッキング](/archive/blogs/tangent_thoughts/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider) をご覧ください。

以下のセクションでは、 Microsoft Dynamics に返される要求に対する重点的なデバッグの手順を示します。

#### <a name="repocapture"></a>リポジトリ/キャプチャ

1. Fiddler を起動し、 **ツール \> オプション \> HTTPS** から **HTTPS トラフィックの復号化** を選択します。
2. トラフィックのキャプチャを開始します (ショートカット キーは F12 キーです)。 ツールの左下を確認すると、該当のトラフィックがキャプチャされていることを確認できます。
3. Internet Explorer の InPrivate モード、またはChrome の Incognito モードを使用して開きます。
4. Finance + Operations を開きます (例 `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`)。
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

    ![個人情報。](media/Scrub-PII.png)

6. 次は、結果が **302** 件ある行を選択します。 URL が、 **.../namespaces/AXSF/** となっていることを確認します。
7. 上記で選択した行に示されているコード行を探してください。 

    ![コード行。](media/Note-the-code.png)

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

タスク マネージャーの各 AOS マシンで、**AXService.exe** を選択し、**タスクの終了** を選択します。

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

- [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#setupvms)
- [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#setupvms)

各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。

また、正しいドメインを使うことを検証する .csv ファイルを確認します。

## <a name="error-runasync-failed-due-to-an-unhandled-fabricexception-causing-replica-to-fault"></a>エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」

次のエラーが表示される場合があります。

> 未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException: 最初の Fabric アップグレードではコード バージョンと設定バージョンの両方を指定する必要があります。 要求された値: 0.0.0.0:

この場合、ClusterConfig.json ファイルで、 **diagnosticsStore** をネットワーク共有からローカル パスに変更します。 たとえば、**\\\\サーバー\\パス** を、規定値の **C:\\ProgramData\\SF\\DiagnosticsStore** に変更します。

## <a name="service-fabric-aos-node-error-during-build-the-execution-time-out-expired"></a>ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ

**エラー:**

> 操作を完了する前にタイムアウト期間が経過したか、サーバーが応答していません。  
> 明細書は終了しました。

一度に 1 つの AOS マシンのみ DB Sync を実行できます。 このエラーは無視しても問題ありません。 AOS VM のいずれかが DB Sync で実行されているため、他の VM が実行できないという警告が表示されたためです。 DB Sync が実行されていることを確認するには、イベント ビューアの、警告を生成していない AOS VM で **アプリケーションおよびサービスのログ** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize/Operational** の順に移動します。

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

- [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#plancert)
- [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#plancert)

## <a name="find-a-list-of-group-managed-service-accounts"></a>グループ管理サービス アカウント の一覧の検索

すべてのグループとホストの一覧を検索するには、次のコマンドを実行します。

```powershell
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

    - [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#joindomain)
    - [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#joindomain)
 
2. すべての AOS コンピューターで、**Config-PreReq** スクリプトを実行します。
3. **テスト構成** スクリプトがパスすることを確認します。
4. UAC が変更された場合は、変更を有効にする前にマシンを再起動する必要があります。

## <a name="files-in-use-errors"></a>使用中ファイルのエラー

「ファイルは使用中です」のエラーが発生した場合は、Service Fabric に示されている例外ルールを設定します。 詳細については、[環境設定](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)を参照してください。

## <a name="apply-deployable-packages-during-deployment"></a>配置中に配置可能パッケージを適用する

### <a name="package-deployment-fails-because-of-a-path-too-long-exception"></a>「パスが長過ぎる」例外によってパッケージの展開が失敗する

Microsoft Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。 文字数の制限を超過した場合、次のエラーが表示されます。

> System.IO.PathTooLongException: 指定されたパス、ファイル名、またはその両方が長すぎます。 完全に記述されたファイル名は 260 文字未満である必要があり、ディレクトリ名は 248 文字未満である必要があります。 at System.IO.PathHelper.GetFullPathName

この問題を回避するには、パッケージ名を短くし、パッケージをもう一度適用します。 または、オンプレミス資産の共有パス全体の長さを短くしてください。

### <a name="package-deployment-fails-because-of-a-serialization-error"></a>シリアル化エラーが原因でパッケージの展開に失敗する

パッケージ配置中、次のエラーが発生する場合があります。

> シリアル化バージョンの不一致が検出されたので、ランタイム DLL が配置されたメタデータと同期していることを確認してください。 「XXX」ファイルのバージョン DLL 「XXX」のバージョン

この場合は、パッケージが開発された環境のバージョンと、パッケージを配置する環境のバージョンが異なっている可能性があります。

この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。 パッケージのアップロード先にあるアセット ライブラリの **追加の詳細** セクションをクリックすることにより、パッケージ バージョンを確認することができます。 このエラーを修正するには、オンプレミス環境に配置されたバージョンと同じか、またはそれ以前のバージョンでパッケージを生成する必要があります。

### <a name="package-deployment-fails-because-of-dependencies-on-missing-modules"></a>欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する

依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次のようなメッセージが表示されます。

> パッケージ \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]
>
> パッケージ \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]
>
> パッケージ \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]

問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーで、**アプリケーションとサービス** を開き、**Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** の順で移動して、見つからないモジュールのあるイベントを表示します。 たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor です。

この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。 依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。 モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除できます。 詳細については、 [モデルのエクスポートとインポート](../dev-tools/models-export-import.md) を参照してください。

### <a name="package-deployment-works-in-a-one-box-environment-but-not-in-the-sandbox-environment"></a>パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない

1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、一方ではサンドボックス環境には実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。 開発環境で作成されたパッケージが、サンドボックス環境ではなく、ワン ボックス環境にあるモジュールに依存する場合、パッケージはサンドボックス環境では動作しません。

この問題を解決するには、依存関係のあるすべてのモジュールを確認し、実稼動環境で不要なアダプターまたはその他のモジュールを使用しないようにしてください。 ビルド ボックスからパッケージを取得することをお勧めします。

## <a name="an-error-occurs-when-you-sign-in-to-on-premises-environments"></a>オンプレミス環境へのログイン時にエラーが発生

- **プラットフォーム更新 12:** **システム管理** \> **設定** \> **クライアント パフォーマンス オプション** に移動して、Skype 統合を無効にしてください。 アプリに移動するとき、`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true` の例のように、**?debug=true** を URL に追加します。
- **プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11:** 確認されている問題は、 Skype の アプリケーション プログラミング インターフェイス (API) が、オンプレミス環境へのサインインする機能に影響を及ぼしているというものです。 Microsoftはこの問題の解決方法を調査しています。 この問題を回避するために、次の例のように URL の末尾に **?debug=true** を追加できます。`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`

## <a name="the-local-agent-stops-working-after-the-tenant-for-the-project-from-lcs-is-changed"></a>ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します

更新されたテナントでローカル エージェントを構成するには、次の手順を実行します。

1. ローカル エージェントをアンインストールします。

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. ユーザーの環境での適切なセットアップと配置トピックの「テナントの LCS 接続のコンフィギュレーション」セクションにある手順を実行します。

    - [プラットフォーム更新 41 以降](setup-deploy-on-premises-pu41.md#configurelcs)
    - [プラットフォームの更新 12 ~ 40](setup-deploy-on-premises-pu12.md#configurelcs)

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

### <a name="plan-and-acquire-your-certificates-as-documented-for-platform-update-42-and-later-or-platform-updates-12-through-40"></a>証明書を計画して取得 ([プラットフォームの更新 42 以降](setup-deploy-on-premises-pu41.md#plancert) または [プラットフォームの更新 12 ~ 40](./setup-deploy-on-premises-pu12.md#plancert) で記載されたものとして)

- 同一のオンプレミスのローカル エージェント証明書を使用する必要があります。
- 同一のスター証明書を使用することができます(AOS SSL および Service Fabric)。
- 残りの証明書は既存の環境の証明書とは異なる可能性があります。

### <a name="download-setup-scripts-from-lcs-as-documented-for-platform-update-42-and-later-or-platform-updates-12-through-40"></a>LCS からのセットアップ スクリプトをダウンロード ([プラットフォームの更新 42 以降](setup-deploy-on-premises-pu41.md#downloadscripts) または [プラットフォームの更新 12 ~ 40](./setup-deploy-on-premises-pu12.md#downloadscripts) で記載されたものとして)

- ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。

### <a name="set-up-a-standalone-service-fabric-cluster-as-documented-for-platform-update-42-and-later-or-platform-updates-12-through-40"></a>スタンドアロンの Service Fabric Cluster を設定 ([プラットフォームの更新 42 以降](setup-deploy-on-premises-pu41.md#setupsfcluster) または [プラットフォームの更新 12 ~ 40](./setup-deploy-on-premises-pu12.md#setupsfcluster) に記載されたものとして)

- ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。

### <a name="configure-lcs-connectivity-for-the-tenant-as-documented-for-platform-update-42-and-later-or-platform-updates-12-through-40"></a>テナントの LCS 接続のコンフィギュレーション ([プラットフォームの更新 42 以降](setup-deploy-on-premises-pu41.md#configurelcs) または [プラットフォームの更新 12 ~ 40](./setup-deploy-on-premises-pu12.md#configurelcs) で記載されたものとして)

- テナントに対して、このタスクを 1 回のみ実行する必要があります。

### <a name="configure-ad-fs-as-documented-for-platform-update-42-and-later-or-platform-updates-12-through-40"></a>AD FS のコンフィギュレーション ([プラットフォームの更新 42 以降](setup-deploy-on-premises-pu41.md#configureadfs) または [プラットフォームの更新 12 ~ 40](./setup-deploy-on-premises-pu12.md#configureadfs) で記載されたものとして)

- [複数環境の同じ AD FS インスタンスの再使用](./onprem-reuseadfs.md) ガイドに従って AD FS を構成します。

## <a name="redeploy-ssrs-reports"></a>SSRS レポートを再配置する

#### <a name="version-10013-or-later"></a>バージョン 10.0.13 、またはそれ以降

ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。

```sql
    UPDATE SF.synclog SET STATE=5, SyncStepName = 'ReportSyncstarted' WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CREATIONDATE DESC)
```

#### <a name="version-10012-or-earlier"></a>バージョン 10.0.12、または以前

ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。

```sql
    DELETE FROM SF.synclog WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CODEPACKAGEVERSION DESC)
```

>[!NOTE]
> バージョン 10.0.12、またはそれ以前のバージョンを使用している場合は、データベース全体が同期されます。

コマンドを実行した後、Service Fabric エクスプローラを使用して AOS ノードの 1 つを再起動するか、ノードが実行されている VM を再起動します。

## <a name="add-axdbadmin-to-tempdb-after-a-sql-server-restart-via-a-stored-procedure"></a>ストアド プロシージャ経由で SQL Server を再起動した後、tempdb に axdbadmin を追加します。

SQL Server を再起動すると、tempdb データベースが再作成されます。 結果として、アクセス許可が不十分です。 マスター データベースでストアド プロシージャを作成する次のスクリプトを実行します。

```sql
\-----
USE [master]
GO
CREATE procedure [dbo].[CREATETEMPDBPERMISSIONS] as begin exec ('USE tempdb; declare @dbaccesscount int; select @dbaccesscount = COUNT(*) from master..syslogins where name = ''axdbadmin''; if (@dbaccesscount <> 0) exec sp_grantdbaccess ''axdbadmin''; ALTER USER [axdbadmin] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''axdbadmin''; EXEC sp_addrolemember N''db_datawriter'', N''axdbadmin''; EXEC sp_addrolemember N''db_ddladmin'', N''axdbadmin''; exec sp_grantdbaccess ''contoso\svc-AXSF$''; ALTER USER [contoso\svc-AXSF$] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_datawriter'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_ddladmin'', N''contoso\svc-AXSF$'';') end
GO
EXEC sp_procoption N'[dbo].[CREATETEMPDBPERMISSIONS]', 'startup', '1'
\-----
```

## <a name="error-updates-to-existing-credential-with-keyid-key-is-not-allowed"></a>エラー : 「KeyId '\<key\>' を使用した既存の資格情報の更新は許可されていません」

次のエラーが表示される場合があります。

> KeyId '\<key\>' を使用した既存の資格情報の更新は許可されていません

この問題を解決するための手順は、オンプレミス プロジェクトのみをご利用しているか、オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用しているかによって異なります。

### <a name="if-have-only-an-on-premises-project"></a>場合設置プロジェクトのみ

オンプレミス プロジェクトのみの場合は、KeyId '\<key\>' を使用して既存の資格情報を更新することはできません。

> New-AzureRmADSpCredential : KeyId '\<key\>' を使用した既存の資格情報の更新は許可されていません。  
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

プラットフォーム バイナリを最新に更新するには、Open Database Connectivity ODBC ドライバー 17 を使用します。 このアップグレードでは、古いバージョンの ODBC ドライバーに関連する安定性の問題を修正します。 [追加の設定](/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites) に関するドキュメントが更新されており、次の変更が記載されています。各AOSサーバーにはODBC ドライバー 17 がインストールされている必要があります。 ODBC ドライバー 17 をインストールしない場合は、環境のメンテナンス処理中に DB 同期エラーが表示されます。

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

## <a name="service-fabric-explorer-warnings-occur-after-you-restart-a-machine"></a>コンピューターの再起動後に Service Fabric Explorer の警告メッセージが表示される

**エラー:**

> エラー: event: SourceId='MonitoringAgentService', Property='ServiceState'.  
> System.Management.Automation.RuntimeException: エラー: **渡された GUID は WMI データ プロバイダーにより有効と認識されませんでした。** (HRESULT からの例外: 0x80071068)。 スタック トレース:

**手順:** この問題を解決するには、警告メッセージの原因であるアプリケーション パッケージを再起動します。 詳しくは、 [アプリケーション(AOS など)を再起動してください](./troubleshoot-on-prem.md#restartapplications) をご覧ください。

## <a name="the-internal-time-zone-version-number-that-is-stored-in-the-database-is-higher-than-the-version-that-is-supported-by-the-kernel-1312"></a>データベースに格納されている内部タイム ゾーンのバージョン番号が、カーネル (13/12) でサポートされているバージョンよりも大きくなっています。

このデータベースの同期エラーにより、新しいビルド (プラットフォーム更新 15) があったデータベースの上に古いプラットフォーム ビルド (プラットフォーム更新 12) が配置されてしまう可能性があります。

この問題を解決するには、 **SYSTIMEZONESVERSION** の値が重要になります。

```sql
select * from SQLSYSTEMVARIABLES where parm = 'SYSTIMEZONESVERSION'
```

エラー メッセージにて表示されたバージョンの値で [value] を更新します

```sql
update SQLSYSTEMVARIABLES set VALUE = 12 where parm = 'SYSTIMEZONESVERSION'
```

## <a name="printing-randomly-stops"></a>印刷がランダムに停止する

AOS サーバーにインストールされているすべてのネットワーク プリンターが、AXService.EXE プロセスが実行されている Windows サービス アカウントとして実行されていることを確認してください。

オンプレミス環境でのネットワーク プリンターの構成方法の詳細については、[オンプレミス環境でのネットワーク プリンター デバイスのインストール](../analytics/install-network-printer-onprem.md) を参照してください。

## <a name="ax-databasesynchronize-isnt-populated-with-events"></a>Ax-DatabaseSynchronize にイベントが設定されていません

プラットフォームの更新 20 およびそれ以降では、データベース同期ログに問題があり、イベント ビューアーで同期ログが **Ax-DatabaseSynchronize** の下に作成されません。

この問題を解決するには、  \<SF-dir\>\\AOS\_\<x\>\\ファブリック\\ワーク\\アプリケーション\\AXSFType\_アプリ\<X\>\\log にアクセスしてください。 例えば次の場所に移動します。 C:\\ProgramData\\SF\\AOS\_11\\Fabric\\work\\Applications\\AXSFType\_App183\\log ここに、Code\_AXSF\_M\_\<X\>.out ファイル内の DatabaseSynchronize からの出力を示します。 このコンポーネントに関する問題をトラブルシューティングします。

## <a name="you-cant-access-finance--operations-aadsts50058-a-silent-sign-in-request-was-sent-but-no-user-is-signed-in"></a>Finance + Operations にアクセスできません: 「AADSTS50058: サイレント サインインの要求が送信されましたが、ログインしているユーザーがいません」

Finance + Operations へのログイン資格情報を入力すると、ブラウザでアプリケーションのレイアウトが少しの間表示されます。 しかしその後、Finance + Operations外部へのリダイレクトを試みた結果、次のエラーが出て失敗します。

> AADSTS50058: サイレント サインイン要求が送信されましたが、ユーザーがログインしていません。

ユーザーのセッションを表すために使用する Cookie が Azure AD への要求で送信されませんでした。 これは、 Internet Explorer または Microsoft Edge を使用している場合で、webアプリケーションが送信しているサイレント サインインのリクエストが Azure AD エンドポイント (login.microsoftonline.com)とは異なる IEのセキュリティ ゾーンに設定されている場合に発生する可能性があります。

この問題を解決するには、次の PowerShell コマンドを実行します。

この問題を解決するには、次の SQL Server query を実行します。

```sql
update [AXDB].[dbo].[SYSCLIENTPERF] set SkypeEnabled = 0
```

または、**クライアント パフォーマンス オプション** ページの **Skype プレゼンスが有効** オプションを無効にします (**システム管理** \> **設定** \> **クライアント パフォーマンス オプション**)。 この方法を使用するには、Finance + Operations にログインできる必要があります。 そのため、最初にブラウザのリダイレクトをブロックする必要があります。 Skypeのプレゼンス機能を無効にすると、リダイレクトのブロックを解除しても構いません。

Chrome ブラウザーでは、最初からリダイレクトがブロックされています。

## <a name="error-there-was-an-error-during-codepackage-activation-service-host-failed-to-activate-error0x8007052e"></a>エラー: CodePackage の有効化でエラーが発生しました。 サービス ホストの有効化に失敗しました。 エラー: 0x8007052e"

新規インストールの際に以下のエラーが発生する可能性があります。

> エラー イベント: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'。 CodePackage の有効化でエラーが発生しました。サービス ホストの有効化に失敗しました。 エラー: 0x8007052e

このエラーと同じエラーが、AXSFサービスでも発生します。

この問題を解決するには、次の手順に従います。

1. [エージェント共有パス](setup-deploy-on-premises-pu12.md#setupfile) にて、 **netstandard.dll** ファイルを見つけます。 このファイルは、例えば \\wp\\\<name\>\\StandaloneSetup-\<ver\>\\Apps\\AOS\\AXServiceApp\\AXSF\\Code\\bin\\netstandard.dll に存在する可能性があります。
2. それぞれの AOS サーバーにて、管理者権限で コマンド プロンプトを開き、次のコマンドを実行します。

    ```Console
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

## <a name="sysclassrunner-doesnt-run-successfully"></a><a name="SysClassRunner"></a>SysClassRunner は正常に実行されません

**問題:** プラットフォーム更新プログラム 29 の SysClassRunner をプラットフォーム更新プログラム 31 を使用して実行しようとすると、次の例外が発生します。

```stacktrace 
Microsoft.Dynamics.Ax.Xpp.ClrErrorException: TypeInitializationExeption ---> 
System.TypeInitializationException: The type initializer for 'Microsoft.Dynamics.Ax.Metadata.XppCompiler.CompilerTracer' threw an exception. ---> 
System.TypeInitializationException: The type initializer for 'Microsoft.Dynamics.Ax.DesignTime.Telemetry.OneDS' threw an exception. ---> 
System.IO.FileLoedAxception: Could not load file or assembly 'Microsoft.Diagnostics.Tracing.TraceEvent, Version=2.0.43.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a' or one of its dependencies. 
The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040) at Microsoft.Dynamics.Ax.DesignTime.Telemetry.OneDS.cctor() 
--- End of inner exception stack trace ---
```

**理由:** ランタイムとアプリケーションとの間に .dll の不一致があります。

**解決策** : TSG\_SysClassRunner.ps1 を使用します。 詳細については、[TSG_SysClassRunner.ps1](onprem-tsg-implementations.md#sysclassrunner)を参照してください。

## <a name="dbsync-fails-with-peap-app-version-1009-platform-update-33"></a>DBSync が PEAP APP バージョン 10.0.9 プラットフォーム更新プログラム 33 で失敗する
**問題:** APP 10.0.9 PU33 PEAP パッケージの配置中に、AXSF アプリケーションの配置が Service Fabric エクスプローラーで「Inbuild」ステータスになると失敗する。 AXSF ノードの作業ディレクトリのログを確認すると、次の DBSync エラーが見つかります。 

DBSync からのエラー メッセージ:
 ```stacktrace
 Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:\ProgramData\SF\LBDEN08FS1AOS03\Fabric\work\Applications\AXSFType_App398\AXSF.Code.1.0.20200123151456\Packages" -metadatadir "C:\ProgramData\SF\LBDEN08FS1AOS03\Fabric\work\Applications\AXSFType_App398\AXSF.Code.1.0.20200123151456\Packages" -sqluser "" -sqlserver "" -sqldatabase "" -setupmode servicesync -syncmode fullall -onprem 
Stack trace: Invalid attempt to call  running in CIL on the client.
   at Microsoft.Dynamics.Ax.MSIL.Interop.throwException(Int32 ExceptionValue, interpret* ip)
   at Microsoft.Dynamics.Ax.MSIL.Interop.ThrowCQLError(IL_CQL_ERR cqlErr, String p1)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.LogOrRethrow(Exception exception)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.LogOrRethrowFormattedMessage(Exception exception, String typeName, String elementName)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.LogOrRethrowFormattedMessage(Exception exception, String typeName, Int32 typeId)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.ApplicationIdBridge.LoadTableById(ApplicationIdBridge* , Int32 id, ObjectIdDelegate* cb)
   at cqlClass.callEx(cqlClass* , Char* , interpret* )
   at Microsoft.Dynamics.Ax.MSIL.cqlClassIL.Call(IntPtr c, String methodName, Object[] parameters, Type[] types, Object[] varargs, Type[] varargsTypes)
   at Microsoft.Dynamics.Ax.Xpp.XppObjectBase.Call(String methodName, Object[] parameters, Type[] types, Object[] varargs)
   at Microsoft.Dynamics.Ax.Xpp.DictTable.Supportinheritance()
   at Dynamics.AX.Application.SysDictTable.`getRootTable(Int32 _tabid) in xppSource://Source/ApplicationPlatform\AxClass_SysDictTable.xpp:line 1498
   at Dynamics.AX.Application.SysDictTable.getRootTable(Int32 _tabid)
   at Dynamics.AX.Application.SysDataBaseLog.`ConfigureSqlLogging() in xppSource://Source/ApplicationPlatform\AxTable_SysDataBaseLog.xpp:line 60
   at Dynamics.AX.Application.SysDataBaseLog.ConfigureSqlLogging()
   at SysDataBaseLog::ConfigureSqlLogging(Object[] , Boolean& )
   at Microsoft.Dynamics.Ax.Xpp.ReflectionCallHelper.MakeStaticCall(Type type, String MethodName, Object[] parameters)
 
DB sync failed.
```

**理由:** この問題が発生するのは、SQL DatabaseLog テーブルに、パッケージ内のメタデータと競合するデータが含まれているためです。

**解決策:** AXDB 上で次のクエリを実行して DatabaseLog テーブルをクリーンアップしてから、配置を再試行します。

```sql
select * into databaselog_bak from databaselog
truncate table databaselog
```

## <a name="dbsync-fails-to-start"></a>DBSync が起動に失敗する

**問題 :** AXSF アプリケーションが Service Fabric explorer で "InBuild" の状態のままとなり、配置が失敗する。 AXSF ノードの作業ディレクトリのログを確認すると、次の DBSync エラーが見つかります。

```stacktrace
Microsoft.Dynamics.AX.InitializationException: Database login failed. Please check SQL credentials and try again.
   at Microsoft.Dynamics.AX.AOS.StartupInternal(String[] Arguments)
   at Microsoft.Dynamics.AX.AOS.Startup()
   at Microsoft.Dynamics.AX.AosConfig.?A0xb5100bbf.GetAosConfig()
   at Microsoft.Dynamics.AX.AosConfig.Config.InitInternal()
   at Microsoft.Dynamics.AX.AosConfig.Config.InitOnce(Boolean isOfflineMode)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.StartAosCode(SyncOptions syncOptions, String sqlConnectionString)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.ExecuteWithinAOS(SyncOptions syncOptions, String sqlConnectionString, IMetadataProvider metadataProvider, Func`1 func, Action`1 errorHandler)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.NOTE_LeavingSynchronizer_CallStackAboveThisLineIsCustomCode(SyncOptions syncOptions, String sqlConnectionString, IMetadataProvider metadataProvider, Action`1 a)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.RunCustomAction(SyncOptions syncOptions, String sqlConnectionString, IMetadataProvider metadataProvider, Action`1 a)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.PreTableSync()
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.FullSync()
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.RunSync()
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.Run(String metadataDirectory, String sqlConnectionString, SyncOptions options)
```

**理由 :** この問題は、SQL パスワードに特殊文字が含まれていることが原因で発生する場合があります。

**解決策 :** SQL ユーザーのパスワードを更新し、特殊文字を削除します。 続いて、新しいパスワードを使用して Credentials.json ファイルを更新し、LCS から配置作業を再試行します。

## <a name="dbsync-fails-with-peap-and-first-release-app-version-10014-platform-update-38"></a>DBSync は PEAP と 初回リリースの APP のバージョン 10.0.14、更新プログラム 38 でエラーが発生する

**問題 :** AXSF アプリケーションが Service Fabric explorer で "InBuild" の状態のままとなり、配置が失敗する。 AXSF ノードの作業ディレクトリでログを確認する場合、以下の DBSync エラーが複数回発生します。

```stacktrace
10/01/2020 14:49:25: Failed when creating deadlock capture session event System.Data.SqlClient.SqlException (0x80131904): User does not have permission to perform this action.
   at System.Data.SqlClient.SqlConnection.OnError(SqlException exception, Boolean breakConnection, Action`1 wrapCloseInAction)
   at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj, Boolean callerHasConnectionLock, Boolean asyncClose)
   at System.Data.SqlClient.TdsParser.TryRun(RunBehavior runBehavior, SqlCommand cmdHandler, SqlDataReader dataStream, BulkCopySimpleResultSet bulkCopyHandler, TdsParserStateObject stateObj, Boolean& dataReady)
   at System.Data.SqlClient.SqlCommand.RunExecuteNonQueryTds(String methodName, Boolean async, Int32 timeout, Boolean asyncWrite)
   at System.Data.SqlClient.SqlCommand.InternalExecuteNonQuery(TaskCompletionSource`1 completion, String methodName, Boolean sendToPipe, Int32 timeout, Boolean& usedCache, Boolean asyncWrite, Boolean inRetry)
   at System.Data.SqlClient.SqlCommand.ExecuteNonQuery()
   at Microsoft.Dynamics.AX.Framework.Database.Monitor.DeadlockMonitor.CreateDeadlockTrackingSystemEvent()
```

**理由:** この問題は、Finance+Operations で使用している SQL Server アカウントに操作を実行するための十分な権限がないことによって発生します。

**解決:** SQL Server で下記のコマンドを実行してください。

```sql
use master
GRANT ALTER ANY EVENT SESSION to axdbadmin;
```

## <a name="reportingservice-fails-to-start"></a>ReportingService が開始できません

**問題:** 展開中に、ReportingService を開始できません。 イベント ログに表示されるエラーは次のとおりです。

```stacktrace
Could not load file or assembly 'Microsoft.SqlServer.BatchParser, Version=12.0.0.0, Culture=neutral, PublicKeyToken=89845dcd8080cc91' or one of its dependencies. An attempt was made to load a program with an incorrect format.
System.Reflection.RuntimeAssembly.GetType(RuntimeAssembly assembly, String name, Boolean throwOnError, Boolean ignoreCase, ObjectHandleOnStack type) 
    at System.Reflection.RuntimeAssembly.GetType(String name, Boolean throwOnError, Boolean ignoreCase) at System.Reflection.Assembly.GetType(String name, Boolean throwOnError)
    at Microsoft.SqlServer.Management.Common.ServerConnection.GetStatements(String query, ExecutionTypes executionType, Int32& statementsToReverse)
    at Microsoft.SqlServer.Management.Common.ServerConnection.ExecuteNonQuery(String sqlCommand, ExecutionTypes executionType)
    at Microsoft.Dynamics.AX.Framework.Reports.Setup.ReportsIdentityUpdater.ExecuteSQlScript(String script)
    at Microsoft.Dynamics.AX.Framework.Reports.Setup.ReportsIdentityUpdater.CreateReportServerDatabase(String userName, SrsWmi rsconfigSetting)
    at Microsoft.Dynamics.AX.Framework.Reports.Setup.ReportsServerInstaller.SetInstanceIdentity(String instanceName, String username)
    at Microsoft.Dynamics.AX.Framework.Reports.Setup.RunReportsSetup.Execute(String path, String encodedConfigurationValues)
```
**理由:** この問題は、正しいバージョンの SSMS がインストールされていないので発生します。 インストールする必要がある SSMS のバージョンは 17.9.1 です。

**解決策:** SSMS バージョン 17.9.1 をインストールします。

## <a name="report-deployment-fails-on-version-10019-and-later"></a>レポートの配置はバージョン 10.0.19 以降で失敗する

**問題:** 配置中にレポートの配置が失敗します。 レポート配置ログに表示されるエラーは次のとおりです。

```stacktrace
Publish-AXReport : Value cannot be null.
Parameter name: The value supplied for parameter 'serviceName' cannot be null or empty.
At C:\ProgramData\SF\AOS12\Fabric\work\Applications\AXSFType_App110\AXSF.Scripts.1.0.20210617153432\Reporting.psm1:492 char:9
+         Publish-AXReport -MaxDegreeOfParallelism 1 -ErrorAction Conti ...
+         ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : OpenError: (Microsoft.Dynam...shReportCommand:PublishReportCommand) [Publish-AXReport], ArgumentNullException
+ FullyQualifiedErrorId : Value cannot be null.
Parameter name: The value supplied for parameter 'serviceName' cannot be null or empty.
Microsoft.Dynamics.AX.Framework.Management.Reports.PublishReportCommand
```

**理由:** AOS は BI ノードで実行されているサービスの一覧を取得して、現在インストールされている SSRS のバージョンを探す必要があります。 AOS を実行するアカウントには、サービスの一覧を取得するための適切なアクセス許可が付与されていないので、失敗して serviceName を取得できません。

**解決策:** LCS の共有資産ライブラリから使用できるインフラストラクチャ スクリプトのバージョン 2.11.1 がリリースされ、これらのアクセス許可が反映され、serviceName が取得可能になります。

> [!NOTE]
> 2.11.0 のインフラストラクチャ スクリプトを使用した場合は、最新バージョンをダウンロードし、次の手順を再度実行します。

#### <a name="automatically-add-these-permissions"></a>次のアクセス許可を自動的に追加します。
1. LCS の共有アセット ライブラリから最新のインフラストラクチャ スクリプトをダウンロードします。
1. 必要に応じて ConfigTemplate.xml を移行します。
1. 管理者特権を持つ PowerShell で次のコマンドを実行します。

    ```powershell
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```
    
1. リモート処理スクリプトを使用しない場合に、生成した VM フォルダを BI ノードにコピーします。
1. 管理者特権を持つ PowerShell で次のコマンドを実行します。

    ```powershell
    # If remoting, execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ForcePushLBDScripts
    .\Complete-PreReqs.ps1
    ```
    
1. 設定を確認するために、管理者特権を持つ PowerShell で次のコマンドを実行します。

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    .\Test-D365FOConfiguration.ps1
    ```

> [!IMPORTANT]
> リモート処理を使用していた場合は、設定の完了後にクリーンアップ手順を実行します。 手順については、[リモート処理が使用された場合、CredSSP を終了処理する](./setup-deploy-on-premises-pu41.md#teardowncredssp) を参照してください。

#### <a name="manually-add-these-permissions"></a>次のアクセス許可を手動で追加します。
1. BI ノードに移動します。
1. lusrmgr.msc (ローカル ユーザーとグループ) を開きます。
1. **Dynamics365ReadServices** という新しいグループを作成します。
1. (axserviceuser、svc-AXSF$ など) で AOS を実行するアカウントを、上で作成したグループに追加します。
1. LCS の共有アセット ライブラリから最新のインフラストラクチャ スクリプトをダウンロードします。
1. インフラストラクチャ スクリプトをBI (SSRS) ノードにコピーします。
1. 次のコンテンツを含む scmgroups.csv ファイルを作成します。

    ```text
    "Name"
    "Dynamics365ReadServices"
    ```
    
1. 管理者特権を持つ PowerShell で次のコマンドを実行します。

    ```powershell
    .\Set-ServiceControlManagerPermissions.ps1
    ```
    
1. 設定を確認するために、管理者特権を持つ PowerShell で次のコマンドを実行します。

    ```powershell
    .\Set-ServiceControlManagerPermissions.ps1 -Test
    ```

## <a name="deployment-fails-on-version-10021-and-later"></a>配置はバージョン 10.0.21 以降で失敗

**問題 :** 配置は失敗し、次のエラーが発生します。

```stacktrace
System.AggregateException: One or more errors occurred. ---> 
LocalAgentCommon.LocalAgentInvalidOperationException: Unable to convert the topology file [\\DC1\D365FFOAgent\assets\topology.xml\088f79e2-3a60-4c2a-9911-c3aadb15959f\7819ab4b-31a1-4738-8ca2-02231239ddbb\Topology.xml] to a valid [config.json]. --->
Newtonsoft.Json.JsonReaderException: Unexpected character encountered while parsing value: F. Path
```

**理由 :** コンフィギュレーションの生成方法はバージョン 10.0.21 で変更されました。

**解決策 :** 新しいコンフィギュレーションを生成するには、ローカル エージェント 2.7.0 以降にアップグレードする必要があります。 使用可能な最新バージョンにアップグレードをお勧めします。

## <a name="add-certtoserviceprincipal-fails"></a>Add-CertToServicePrincipal 失敗

**問題 :** 次のエラーが発生し、予期せず実行が終了します。

```stacktrace
Where-Object : Cannot convert null to type "System.DateTime".
At C:\InfrastructureScripts\Scripts\Add-CertToServicePrincipal.ps1:93 char:44
+ ... edentials | Where-Object {[datetime]$_.EndDate -eq $localAgentCertEnd ...
+                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   + CategoryInfo          : InvalidArgument: (:) [Where-Object], RuntimeException
   + FullyQualifiedErrorId : nullToObjectInvalidCast,Microsoft.PowerShell.Commands.WhereObjectCommand
```

**理由 :** Azure PowerShell モジュールのバージョン 7.0 には、スクリプトと互換性がない新しい変更が導入されています。

**解決策 :** Azure PowerShell モジュールのバージョンを、バージョン 6.6.0 にダウングレードします。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
