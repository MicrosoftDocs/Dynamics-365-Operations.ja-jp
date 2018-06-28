---
title: "Dynamics 365 for Finance and Operations (オンプレミス) のトラブルシューティング"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations におけるオンプレミス展開のトラブルシューティング情報を提供します。"
author: sarvanisathish
manager: AnnBe
ms.date: 03/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: f05da8a79dd07fcd8bf98bfd8a5e510d81b61384
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="troubleshoot-dynamics-365-for-finance-and-operations-on-premises"></a>Dynamics 365 for Finance and Operations (オンプレミス) のトラブルシューティング

[!INCLUDE [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations におけるオンプレミス展開のトラブルシューティング情報を提供します。

## <a name="error-when-signing-in-to-on-premises-environments"></a>オンプレミス環境へのログイン時のエラー

PU12 [システム管理] > [設定] > [クライアントのパフォーマンス フォーム オプション] に移動して、"Skype 統合" を無効にしてください。
アプリに移動するとき、https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true の例のように、?debug=true を追加します。

PU8 および PU11 オンプレミス環境へのサインイン機能に影響を与える Skype API の問題が検出されました。 この問題の解決方法を調査しています。 しばらくは、この問題を回避するために、次の例のように URL の末尾に **?debug = true** を追加できます。

`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`

## <a name="service-fabric"></a>Service Fabric 
Service Fabric は、オンプレミス展開のためにインストールおよび構成する初期コンポーネントの 1 つです。 Service Fabric は、オーケストレータ、Application Object Server (AOS)、SSRS、および MR ノードで使用されます。

## <a name="access-service-fabric-explorer"></a>Service Fabric Explorer へのアクセス
Service Fabric Explorer には、ブラウザーと既定のアドレス https://sf.d365ffo.onprem.contoso.com:19080 を使ってアクセスできます。

アドレスを確認するには、[DNS ゾーンの作成] セクションで使用した内容をメモし、環境に適したトピックに A レコードを追加します。 
- [プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#createdns).
- [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#createdns)

サイトにアクセスするには、クライアント証明書がサイトにアクセスしているマシンの `cert:\CurrentUser\My` (**証明書 - 現在のユーザー** > **個人** > **証明書**) にある必要があります。 サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。

## <a name="locate-logs-for-deployment-diagnostics"></a>配置の診断のログを検索します。

LocalAgent が稼動する各オーケストレーター マシンの責任を調べるには、[[ログ レビューのためのノードの特定方法]](#stateful-and-stateless-services-how-to-identify-nodes-for-log-review) セクションを参照してください。

### <a name="deployment-failure-logs"></a>配置の失敗ログ

#### <a name="orchestrator-machine-failures"></a>オーケストレータ コンピューター エラー

展開中の `fabric:/LocalAgent/ArtifactsManager` および `fabric:/LocalAgent/OrchestrationService` 下の主要なノードは、最上位の利息です。 それぞれで、イベント ビューアーを開き、展開済みの配置プロセスに関する情報およびエラーについては、`Applications and Services Logs\Microsoft\Dynamics\AX-LocalAgent\Operational` に移動してください。

特に、`OrchestrationService` の場合、次のイベントの場所は AX のインストール中に展開に失敗した場合に調査する必要があります: `Applications and Services Logs\Microsoft\Dynamics\AX-SetupModuleEvents\Operational`。

#### <a name="ax-deployment-failures"></a>AX の配置の失敗

AX が Service Fabric で "InBuild" のときは、データベースが最新の状態ではないことが検出された場合、AX は DbSync を実行します。 DbSync は、さまざまな理由で失敗する可能性があります。その多くについてはこの記事で扱います。

DbSync エラーを診断するには、`Applications and Services Logs\Microsoft\Dynamics\AX-DatabaseSynchronize\Operational` にあるイベント ログを参照してください。 エラーの詳細は、この記事で役立つセクションを見つけるのに役立ちます。

## <a name="stateful-and-stateless-services-how-to-identify-nodes-for-log-review"></a>ステートフルおよびステートレス サービス。ログ レビューのノードを識別する方法
どんなマシンがローカル エージェントのようなステートフル サービスのプライマリ インスタンスであるかを確認するには、Service Fabric Explorer を開き、**クラスタ** > **アプリケーション** > **(目的のアプリケーション ex) LocalAgentType** > **fabric:/LocalAgent** > **Fabric:/LocalAgent/ArtifactsManager** > **(guid)** を展開します。

プライマリ ノードに注意してください。 ステートレス サービス、または他のアプリケーションについては、すべてのノードを確認する必要があります。

## <a name="timeout-error-received-when-creating-a-service-fabric-cluster"></a>Service Fabric クラスターの作成時に受信したタイムアウト エラー
該当するセットアップ トピックにあるスタンドアロン Service Fabric クラスターのセットアップにあるように Test-D365FOConfiguration.ps1 を実行し、エラーに注目します。 
- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#setupsfcluster)
- [プラットフォーム更新プログラム 8 および 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)

すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。
Service Fabric Server 証明書にすべての Service Fabric ノード上のネットワーク サービス 用 ACL が含まれていることを確認します。

## <a name="time-out-while-waiting-for-installer-service-to-complete-for-machine-xxxx"></a>インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウトしました
IP アドレス (マシン) ごとにノード タイプを 1 つのみ持つことができます。 ノードが同じマシン上で再利用されているかどうかを確認してください。 たとえば、AOS および ORCH は、同一のマシン上にある必要があり、ConfigTemplate.xml が正しく定義される必要があります。

## <a name="remove-a-specific-application"></a>特定のアプリケーションを削除
配置の削除またはクリーンアップに Lifecycle Services (LCS) を使用することをお勧めします。 ただし、追加の手順が必要な場合は、アプリケーションを削除する Service Fabric Explorer を使用できます。

Service Fabric エクスプローラーで、**アプリケーション ノード** > **アプリケーション** > **MonitoringAgentAppType-Agent** に移動します。 **ファブリック:/エージェント監視**で省略記号をクリックし、アプリケーションを削除します。 確認のためにアプリケーションの正式名称を入力します。
また、省略記号および **非引当タイプ** の順にクリックすることにより、**MonitoringAgentAppType-Agent** を削除することができます。 確認のために正式名称を入力します。

### <a name="remove-all-ax-applications-from-service-fabric"></a>Service Fabric からすべての AX アプリケーションを削除

次のスクリプトは、LocalAgent および LocalAgent の Monitoring エージェントを除く、すべての SF アプリケーションを削除およびプロビジョニング解除します。 これは、オーケストレータ VM で実行する必要があります。

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
Service Fabric クラスターを完全に削除するには、次のコマンドを実行します。

```powershell
.\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
```

これによりエラーが発生する場合は、ノードで次のスクリプトを使用してそのクラスターで特定のノードを削除します。

```powershell
& "C:\Program Files\Microsoft Service Fabric\bin\fabric\fabric.code\CleanFabric.ps1"
```

次に、既定値を使用する場合、`C:\ProgramData\SF` のフォルダーを削除します。 それ以外の場合、指定したフォルダーを削除します。
アクセス拒否エラーが発生した場合は、PowerShell を再起動するか、マシンを再起動します。

## <a name="clean-up-an-existing-environment-and-start-over"></a>既存の環境をクリーンアップしてやり直す

最初からやり直すために、以下の手順に従います。

1. LCS のプロジェクトへのアクセス。
    1. [環境] で、展開を削除します。
    1. アプリケーションが環境の Service Fabric Explorer から表示されなくなることに注意してください。 これには 1 〜 2 分かかります。
2. `LocalAgentCLI.exe` を含むオーケストレーター マシンへのアクセス。
   1. ローカル エージェント クリーンアップを実行します。
       ```powershell
       .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
       ```
   2. Service Fabric の削除:
       ```powershell
       .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath '<path of ClusterConfig.json>'
       ```
   3. いずれかのノードが Service Fabric をアンインストールするのに失敗した場合は、各障害が発生したノードに対して、次を実行します。
       ```powershell
       & "C:\Program Files\Microsoft Service Fabric\bin\fabric\fabric.code\CleanFabric.ps1"
       ```
   4. すべての Service Fabric ノードの `C:\ProgramData\SF\` フォルダーを削除します。
       - アクセスが拒否された場合は、マシンを再起動してからやり直します。
3. 証明を削除します。
   1. すべての AOS、BI、ORCH、および DC ノードから古い証明書を削除します。
       - 証明書は、次の証明書ストアに存在します。`Cert:\CurrentUser\My\`、`Cert:\LocalMachine\My` および `Cert:\LocalMachine\Root`。
   2. SQL サーバー設定が変更される場合は、SQL サーバー証明書も削除します。
   3. ADFS 設定が変更される場合は、ADFS 証明書を削除します。

4. 更新プログラム構成ファイル。 テンプレートのフィールドを適切に入力するには、[プラットフォーム更新 12](setup-deploy-on-premises-pu12.md) または[プラットフォーム更新8 または 11](setup-deploy-on-premises-pu8-pu11.md) の該当する展開ドキュメントをご覧ください。 
    - ConfigTemplate.xml
    - ClusterConfig.json
5. LCS のプロジェクトへのアクセス。
    1. 環境の LCS コネクタを再作成するか、または既存のコネクタの設定を編集します。
        - LCS の値を簡単にコピーするには、`.\Get-AgentConfiguration.ps1`script を使用します。
    1. 最新のローカル エージェント コンフィギュレーション `localagent-config.json` をダウンロードします。

ここで、[プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md) または[プラットフォーム更新プログラム 8 または 11](setup-deploy-on-premises-pu8-pu11.md) の適切な配置のドキュメントから再び開始します。

## <a name="local-agent"></a>ローカル エージェント
ローカル エージェントは、LCS との通信、インストールするコンポーネントのダウンロード、Dynamics 365 for Finance and Operations のインストール、管理、削除を担当するフレームワークです。

## <a name="how-to-find-the-local-agent-values-that-are-used"></a>使用するローカル エージェント値を検索する方法
ローカル エージェントの値は、**クラスター** > **アプリケーション** > **LocalAgentType** > **fabric:/LocalAgent、詳細/** の Service Fabric Explorer で確認できます。

## <a name="install-upgrade-or-uninstall-local-agent"></a>ローカル エージェントのインストール、アップグレード、アンインストール
ローカル エージェントのインストールは、適切なプラットフォーム更新プログラムに関するオンプレミス環境の設定と配置で説明します。 
- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md) 
- [プラットフォーム更新プログラム 8 もしくは 11](setup-deploy-on-premises-pu8-pu11.md)

また、以下のアップグレードおよびアンインストール コマンドを使用することができます。

```powershell
LocalAgentCLI.exe Install <path of localagent-config.json>
LocalAgentCLI.exe Upgrade <path of localagent-config.json>
LocalAgentCLI.exe Cleanup <path of localagent-config.json>
```

> [!NOTE]
> クリーンアップ コマンドは、ファイル共有に配置されたファイルを削除しません。 ファイル共有は再利用できます。

## <a name="error-occurs-when-starting-up-local-agent-services"></a>ローカル エージェント サービスを開始するときにエラーが発生
「'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' というファイルまたはアセンブリ、またはその依存関係のいずれかをロードできませんでした」というエラーが発生した場合、**厳密な名前**検証は有効化できなくなります。 これは、Configure-PreReqs.ps1 を使用して行います。 検証が有効になっていないことを確認するには、Test-D365FOConfiguration.ps1 を実行します。

## <a name="validation-in-progress-message-displays-for-several-minutes-in-lcs"></a>「検証が進行中」のメッセージが LCS に数分表示されます。
ローカル エージェントの検証に関する一般的な問題をトラブルシューティングするには、次の手順を実行します。
1. コンピューターを正しくコンフィギュレーションするすべてのオーケストレータ機械で Configure-PreReqs.ps1 を実行します。
2. Test-D365FOConfiguration.ps1 スクリプトがすべての Orchestrator マシンで通ることを確認します。
3. LocalAgentCLI.exe のインストールが正常に完了したことを確認します。
4. Service Fabric Explorer に移動し、アプリケーションがすべてが正常であることを確認します。
5. アプリケーションが正常な場合は、障害が発生したサービスの基本ノードを探します。 次からイベントを検索します。
    - **イベント ビューアー** > **カスタム ビュー** > **管理イベント**
    - **イベント ビューアー** > **アプリケーションおよびサービス ログ** > **Microsoft** > **Dynamics** > **AX-LocalAgent**

**一般的なエラー**

次のような一般的なエラーが発生する可能性があります。

- 「コマンドを処理できません」または「チャンネル情報を取得できません」
- 「ホスト プロセスがクラッシュする処理されない例外が原因で RunAsync が失敗しました: System.ArgumentNullException: 値を null にすることはできません。 パラメーター名: 証明書"

**理由** これらのエラーは、OnPremLocalAgent 証明書に指定された証明書が有効でないか、テナントに対して正しく構成されていないために発生することがあります。

**ステップ**エラーを解決するには、次の手順を完了してください。
1. すべてのオーケストレータ ノードで Test-D365FOConfiguration.ps1 を実行し、すべてのチェックに合格することを確認します。
2. ローカル エージェント コンフィギュレーションに指定された証明書が正しいことを確認します。
    - LCS および ConfigTemplate.xml で拇印を指定する際に、特殊文字がないことを確認します。
    - 証明書は、次のような infrastructure\ConfigTemplate.xml で指定されているものと同じである必要があります。

        ```xml
        <Certificate type="Orchestrator" exportable="true" generateSelfSignedCert="true">
            <Name>OnPremLocalAgent</Name>
            <Thumbprint></Thumbprint>
            <ProtectTo></ProtectTo>
        </Certificate>
        ```

3. テナント用 LCS 接続のコンフィギュレーションが、LCS のローカル エージェントコンフィギュレーションで指定されているのと同じ証明書を使用して完了したことを、確認します。 
    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#configurelcs)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs)
4. ローカル エージェントをアンインストールします。
5. ローカル エージェント コンフィギュレーションで正しい証明書を指定し、もう一度コンフィギュレーション ファイルをダウンロードします。
6. 新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。

**エラー** `'\\...\agent\assets\StandAloneSetup-76308-1.zip'` パスへのアクセスは拒否されます。

**理由** ローカル エージェント コンフィギュレーションで指定されたファイル共有が無効です。

**ステップ**エラーを解決するには、次の手順を完了してください。
1. 指定した共有が存在することを確認します。
2. ローカル エージェント ユーザーが共有への完全なアクセス許可を持っていることを確認します。 ローカル エージェント ユーザーは、次のセクションの ConfigTemplate.xml で指定された DNS 名です。

    ```xml
    <ADServiceAccount type="gMSA" name="svc-LocalAgent$" refName="gmsaLocalAgent">
        <DNSHostName>svc-LocalAgent.d365ffo.onprem.contoso.com</DNSHostName>
    </ADServiceAccount>
    ```

3. 設定文書の設定ファイル共有セクションが完了したことを確認します。
4. ローカル エージェントをアンインストールします。
5. ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。
6. 新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。

**エラー**ユーザー「D365\svc LocalAgent$」へのログインが失敗しました。 理由: 指定した名前に一致するログインが見つかりませんでした。 [CLIENT: 10.0.2.23]

**理由** ローカル エージェント ユーザーはオーケストレーション データベースに接続できません。 これは、ユーザーが削除されて AD で再作成された可能性があるために発生します。つまり、ユーザーの SID が変更されたことを意味します。 SQL Server またはデータベースのユーザーに与えられたアクセスは機能しなくなります。

**ステップ**エラーを解決するには、次の手順を完了してください。

1. SQL Server でスクリプトを実行します。
    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    空の Orchestrator データベースが存在しない場合は作成され、db\_owner 権限を持つデータベースにローカル エージェント ユーザーが追加されます。

2. アプリケーションは、適切なアクセス許可が付与された後は、自動的に正常な状態になります。
3. SQL FQDN、データベース名、およびローカル エージェント ユーザーなどの、設定のいずれかが LCS に正しく記載されていない場合、設定を変更し、ローカル エージェントを再インストールします。
4. 最初の 3 つの手順を実行しても問題が解決しない場合は、SQL server とデータベースからローカル エージェント ユーザーを手動で削除し、初期化データベース スクリプトを再実行します。
5. AD でユーザーを再作成する場合、SID は変更されないことを留意します。 ユーザーの以前の SID を削除し、新しい SID を追加します。

**追加シナリオ**ローカル エージェント ユーザーは、SQL Server またはデータベースに接続できません。

**ステップ**エラーを解決するには、次の手順を完了してください。

1. SQL Server のプライマリ ノード データベースから svc-LocalAgent ユーザーを削除し、両方のサーバーからログインを削除します。
2. 次のスクリプトを実行します。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

   これらのスクリプトは、**常時オン**設定では機能しません。 データベースは、最初にプライマリ ノードで作成し、その後、複製する必要があります。

**エラー** RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。 ---> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'

**理由** ローカル エージェントマシンは lcsapi.lcs.dynamics.com に接続できません。AX-BridgeService のイベントログで「リモート名を解決できませんでした: lcsapi.lcs.dynamics.com」を確認してください。

**ステップ**エラーを解決するには、次の手順を完了してください。
1. `psping lcsapi.lcs.dynamics.com:80` を実行します。
2. 応答を受信しない場合は、組織の IT 部門に問い合わせます。 ファイアウォールが lcsapi またはプロキシの問題へのアクセスをブロックしています。

        lcsapi.lcs.dynamics.com:443
        login.windows.net:443
        uswelcs1lcm.queue.core.windows.net:443
        www.office.com:443
        login.microsoftonline.com:443
        dc.services.visualstudio.com:443
        uswelcs1lcm.blob.core.windows.net:443
        uswedpl1catalog.blob.core.windows.net:443 

## <a name="error-unable-to-load-dll-fabricclientdll"></a>エラー、「DLL 'FabricClient.dll' を読み込むことができません」
このエラーが発生した場合は、閉じて、PowerShell を再表示します。 エラーがまだ発生する場合は、コンピューターを再起動します。

## <a name="what-cluster-id-in-agent-config-should-be-used"></a>エージェント構成でどのようなクラスター ID を使用する必要がありますか
クラスター ID は、任意の GUID にすることができます。 この GUID は、追跡目的で使用されます。

## <a name="local-agent-stops-working-after-the-tenant-for-the-project-from-lcs-is-changed"></a>ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します
更新されたテナントでローカル エージェントを構成するには、以下の手順を実行します。
1. 既にコネクタがインストールされている LCS からすべての環境を削除します。
2. ローカル エージェントをアンインストールします。

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

3. 手順 11 の手順を実行します。 環境のテナントに LCS 接続をコンフィギュレーションします。
    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#configurelcs)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

4. 新しいテナントに新しい LCS コネクタを作成します。
5. local-agent.config file をダウンロードします。
6. ローカル エージェントをインストールします。

    ```powershell
    .\LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

## <a name="monitor-deployment-locally"></a>ローカルでの配置の監視
プライマリ オーケストレータ コンピューターとコンポーネント マネージャー、およびブリッジ サービス AX LocalAgent (全体的なインストール プロセス) のイベント ビューアー ログを確認します。

- モジュール
    - 共通
    - Reportingservices
    - AOS
    - Financialreporting
- コマンド
    - 段取り
    - Dvt - 配置確認テスト

AX SetupModuleEvents (モジュールの追加の詳細情報) AX SetupInfrastructureEvents (Service Fabric との対話がある場合の追加の詳細)

## <a name="aos-machines"></a>AOS マシン
**イベント ビューアー** > **アプリケーションとサービス ログ** > **Microsoft** > **Dynamics** > **AX DatabaseSynchronize**
**イベント ビューアー** > **カスタム ビュー** > **管理イベント**

## <a name="to-view-the-entire-error-message"></a>エラー メッセージ全体を表示するには
**詳細** タブをクリックし、完全なエラー メッセージを表示します。

## <a name="service-fabric-failing"></a>Service Fabric の障害
失敗しているサービスをメモして、対応するアプリケーション ディレクトリを開きます。 例: `C:\ProgramData\SF\<OrchestratorMachineName>\Fabric\work\Applications\LocalAgentType_App<N>\log`

## <a name="encryption-errors"></a>暗号化エラー
暗号化エラーの例には、AXBootstrapperAppType、Bootstrapper、AXDiagnostics、RTGatewayAppType、ゲートウェイの潜在的なエラー関連、Microsoft.D365.Gateways.ClusterGateway.exe などがあります。

データの暗号化証明書がマシンにインストールされていない AOS AccountPassword を暗号化するために使用される場合、これらのエラーのいずれかを受け取る可能性があります。 この証明書が証明書 (ローカル コンピューター) に存在する可能性があります。または、プロバイダーの種類が間違っている可能性があります。

エラーを解決するには、credentials.json ファイルを検証します。 次のメッセージを (AOS1 上に) 入力することによって、テキストの暗号化が正しく解除されていることを確認します。

```powershell
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

このエラーは、パラメーター **''** が ApplicationManifest ファイルで定義されていない場合にも発生する可能性があります。 これを確認するには、**イベント ビューア** > **ユーザー設定ビュー** > **管理イベント** に移動し、次を確認します。

- credentials.json ファイルの適切なレイアウト/構造は、資格情報を暗号化します。 詳細については、「環境の資格情報の暗号化」を参照してください。
    - [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#encryptcred)
    - [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#encryptcred)
- 行末または次の行での終了引用符です。
- Microsoft-Service Fabric ソースでエラーが発生しました。

## <a name="properties-to-create-a-dataencryption-certificate"></a>DataEncryption 証明書を作成するためのプロパティ
DataEncryption 証明書を作成するのにには、次のプロパティを使用します。

- **自己署名証明書:** 自己署名証明書を使用する場合にのみ有効にします。
- **証明書の目的:** この証明書のすべての目的を有効にします。
- **署名アルゴリズム:** sha256RSA
- **署名ハッシュ アルゴリズム:** sha256
- **発行者:** CN = DataEncryptionCertificate
- **公開キー:** RSA (2048 ビット)
- **拇印アルゴリズム:** sha1

> [!WARNING]
> 製造環境では、自己署名証明書を使用しないでください。 代わりに、証明書機関によって発行された証明書を使用します。

## <a name="cant-find-the-certificate-and-private-key-to-use-for-decryption-0x8009200c"></a>暗号の解読に使用する証明書と秘密キーを見つけることができません (0x8009200C)
証明書と ACL がない場合、または間違った拇印エントリがある場合は、特殊文字を確認し、拇印に対して `C:\ProgramData\SF\<AOSMachineName>\Fabric\work\Applications\AXBootstrapperAppType_App<N>\log\ConfigureCertificates-<timestamp>.txt` をチェックインします。
また、`Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard` を使用してテストすることができます。 「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACL を確認します。

Credentials.json が変更された場合は、削除し、LCS から再配置します。

上のどれも動作しない場合:

1. ConfigTemplate.xml で指定されたドメイン名と AD アカウント名前が正しいことを確認します。
1. 用意されたスクリプトを使用して証明書が生成されなかった場合に ConfigTemplate.xml で指定された拇印が正しいことを確認します。
1. LCS で指定された証明書の拇印が正しく、ConfigTemplate.xml で指定されたものと一致することを確認します。 特殊文字がないことを確認します。 `.\Get-DeploymentSettings.ps1` を実行して、コピーしやすい方法で拇印を取得することができます。
1. 証明書が生成されない場合、確認プロバイダー名は、次の証明書タイプと一致します。
    - ServiceFabricEncryption - Microsoft Enhanced Cryptographic Provider v1.0
    - その他のすべての証明書タイプ - Microsoft の拡張された RSA および AES 暗号化プロバイダー
1. `Set-CertificateAcls.ps1` および `Test-D365FOConfiguration.ps1` スクリプトが Service Fabric マシンで正常に実行されたことを確認します。
1. `credential.json` が存在し、エントリが適切な値に復号化されていることを確認します。
    1. AOS マシンのいずれかに移動します。
    1. データ暗号化証明書が正しいことを確認するためのコマンドを実行します。

        ```powershell
        Invoke-ServiceFabricDecryptText '<encrypted string>' -StoreLocation LocalMachine
        ```
1. 変更するために必要な証明書のいずれかまたはコンフィギュレーションが間違っていた場合:
    1. 正しい値で、ConfigTemplate.xml を編集します。
    1. すべてのセットアップ スクリプトと Test-D365FOConfiguration を実行します。
    LCS に戻り、環境を再コンフィギュレーションします。

## <a name="mr"></a>MR
追加のログは、プロバイダーを登録することで実行できます。 [ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) をプライマリ オーケストレータ マシンにダウンロードし、次のコマンドを実行します。

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"}
```

登録を解除する必要がある場合は、次のコマンドを使用します。

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"} -Unregister
```

プロバイダーが登録されると、追加の詳細は、**イベント ビューア** > **アプリケーションとサービス ログ** > **Microsoft** > **Dynamics** の新しい配置について記録されます。

- MR-Logger
- MR-Sql

### <a name="error-while-executing-addaxdatabasechangetracking"></a>AddAXDatabaseChangeTracking の実行中のエラー
AddAXDatabaseChangeTracking を Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess (DeploymentCmdlet) での実行中にエラーが発生した場合は、フル パスが正しいことを確認します。 たとえば、ax.d365ffo.onprem.contoso.com。エラーはスター/* 証明書の問題が原因で発生した可能性があります。 たとえば、リモート証明書 CN=\*.d365ffo.onprem.contoso.com には、無効なまたはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。

### <a name="remote-name-cant-be-resolved"></a>リモート名を解決できません
リモート名を解決できませんでした。'x.d365fo.onprem.contoso.com' / メッセージを承認できなかった https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService をリッスンしていたエンドポイントはありませんでした。 これは、しばしば正しくないアドレスまたは SOAP アクションによって引き起こされます。 URL を手動で参照することによってアドレスに到達可能なことを確認します。 詳細については、存在する場合は InnerException を参照してください。

### <a name="run-initialize-database-script-and-validate-dbs-have-correct-users"></a>データベース初期化スクリプトを実行し、DB のユーザーが適切であることを検証
AddAXDatabaseChangeTracking イベントのみを受け取った場合は、https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService にアクセスし、Dynamics 365 for Finance and Operations の Metadataservice にアクセスしてみてください。
次に、wif.config ファイルでサービスの証明書を確認します。 ファイルを検索するには、AOS ボックスにログオンし、タスク マネージャを使用して **AxService.exe** を右クリックし、**ファイルの場所を開く** を選択します。 wif.config ファイルでは、3 つの拇印を確認する必要があります。 これらの拇印に関する次の要件に注意してください。

- これらは別にする必要があります。
- これらは、この順序である必要があります。
    1. Financialreporting 拇印
    2. ReportingService 拇印
    3. SessionAuthentication 拇印

拇印が要件のリストにない場合は、適切な拇印で LCS から再展開する必要があります。

## <a name="axdbadmin-is-unable-to-connect-to-the-database-server-sql-lscontosocom"></a>axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。

理由: AX データベースに接続するためのアクセス許可がありません。

解決する手順:

1. 既に存在する場合はデータベースから axdbadmin ユーザーを削除します。
2. ConfigTemplate.xml ファイルの AX データベースに追加する必要があるユーザー名を指定してください。
    ```xml
    <Security>
        <User refName="axdbadmin" type="SqlUser" userName="axdbadmin" />
    </Security>
    ```
3. axdbadmin ユーザーを追加するには、もう一度初期化データベース スクリプトを実行します。

## <a name="unable-to-resolve-the-xpath-value"></a>xPath 値を解決することができません。
[TopologyInstance/CustomizationGroup[@name='ServiceConfiguration']/Group[@name='AOSServicePrincipalUser']/Customizations/Customization[@"fieldName="'PrincipalUserAccountPassword']/@selectedValue の xPath 値を解決できないことは、期待される動作であり問題ではありません。 xPath 値は AOS ランタイム ユーザー情報を検索しますが、セキュリティが統合されているため、情報は必要ありません。 別の理由でエラーを調査する必要がある場合は、xPath を解決できないことが通知されます。

## <a name="adfs"></a>ADFS
### <a name="login-page-not-redirecting"></a>リダイレクトしないログイン ページ
ログイン ページがリダイレクトされず、資格情報の入力を求められている場合、またはリダイレクトされているが、"エラーが発生しています" というメッセージを受信する場合。 詳細については、管理者にお問い合わせください」は、次の操作を実行して問題を解決できます。

- 信頼済サイトに ADFS リンクを追加します。
- 信頼済サイトに Dynamics 365 リンクを追加します。
- 末尾にスラッシュ「/」を追加して、動作が変更されるかどうかを確認します。

**ADFS** > **アプリケーション グループ** に順に移動して、AD FS マネージャーを確認します。 **Microsoft Dynamics 365 for Operations on-premises** をダブルクリックします。 **ネイティブ アプリケーション** で、**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション** をダブルクリックします。
- リダイレクト URI に注意してください。 Finance and Operations の DNS 前方参照ゾーンに一致させる必要があります。

### <a name="error-could-not-establish-trust-relationship-for-the-ssltls-secure-channel"></a>エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」
「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」というエラーが表示された場合は、次の操作を行います。

1. **Service Fabric** > **クラスタ** > **アプリケーション** > **AXSFType** > **fabric:/AXSF** > **詳細**タブの順に移動し、 Aad\_AADMetadataLocationFormat / - Aad\_FederationMetadataLocation に移動します。 次に、AOS からその URL を参照します。
2. 詳細については、**AOS イベント ビューアー** > **アプリケーションとサービス ログ**s > **Microsoft** > **Dynamics** > **AX-SystemRuntime** の順に移動します。
3. ADFS 証明書が信頼されているかどうかを確認します。
    1. **ADFS マシン** > **サーバー マネージャー** > **ツール** > **AD FS 管理** に移動して、ADFS 証明書を確認します。
    2. **AD FS** > **サービス** > **証明書**展開し、証明書を注記します。 たとえば、ex。 dc1.contoso.com.
    3. AOS コンピューターで、証明書マネージャーに移動し、**証明書** (ローカル コンピューター) > **信頼済ルート証明機関** > **証明書**および ADFS 証明書が表示されていることを確認します。
サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていないからです。

### <a name="cant-connect-to-remote-server-in-some-locations"></a>一部の地域ではリモート サーバーに接続できません
次の場所でリモート サーバーに接続することはできません。

- System.Net.HttpWebRequest.GetResponse()
- System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)
- System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn) `C:\ProgramData\SF\AOS_1\Fabric\work\Applications\AXSFType_App35\log` フォルダーに移動すると、エラーおよび出力ファイルがあります。
out ファイルには、次の情報が含まれます。

- System.Net.WebException: リモート サーバーに接続できません --->
- System.Net.Sockets.SocketException: 接続した当事者が一定時間適切に応答しなかったため接続試行に失敗したか、接続したホストが x.x.x.x:443 に応答できなかったため確立された接続に失敗しました

Psping を使用してリモート サーバーに対する接続を試みることもできます。 Psping の詳細については、[Psping](/sysinternals/downloads/psping) を参照してください。

### <a name="redirect-login-questions-and-issues"></a>ログイン時の質問および問題をリダイレクト
ログインに問題が発生した場合は、Service Fabric Explorer で **Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** が有効であることを確認します。 次にその例を示します。

- **Provisioning\_AdminPrincipalName** は AXServiceUser@contoso.com になります
- **Provisioning\_AdminIdentityProvider** は https://DC1.contoso.com/adfs になります

有効でない場合は、続行することはできませんし、LCS から再配置する必要があります。

**Reset-DatabaseUsers.ps1** を使用した場合、変更内容を有効にするには、Dynamics サービスを再起動する必要があります。 ログインの問題がまだある場合は、**USERINFO** テーブルで、**NETWORKDOMAIN** および **NETWORKALIAS** を記録します。 次にその例を示します。

- NETWORKDOMAIN の例 https://DC1.contoso.com/adfs
- NETWORKALIAS の例 AXServiceUser@contoso.com

ADFS マシンで、**サーバー マネージャー** > **ツール** > **AD FS の管理** > **サービス**に移動します。 **フェデレーション サービス プロパティの保守と編集** を右クリックします。 フェデレーション サービスの識別子は、**USERINFO.NETWORKDOMAIN (https://DC1.contoso.com/adfs)** と一致させる必要があることに注意してください。 両方とも **USERINFO** の HTTPS であることを確認します。

ADFS マシンで、**イベント ビューアー** > **アプリケーションとサービス ログ** > **AD FS** > **管理者**に移動してエラーを確認します。

## <a name="login-issues"></a>ログインの問題
ユーザーや他のユーザーがログインの問題を経験している場合は、Service Fabric Explorer で Provisioning\_AdminPrincipalName および Provisioning\_AdminIdentityProvider が有効であることを確認します。 有効な場合は、主要 SQL Server マシンで次を実行します。

```powershell
.\Reset-DatabaseUsers.ps1
```

各 AOS で、タスク マネージャーを開き、AXService.exe を選択し、**タスクの終了**をクリックします。
ユーザーがリセットされたことを確認するには、SQL AXDB で次の select クエリを実行します。

```sql
select SID, NETWORKDOMAIN, NETWORKALIAS, * from AXDB.dbo.USERINFO where id = 'admin'
```

> [!NOTE]
> AAD 環境 (オンライン) の SID は、ネットワーク エイリアスとネットワーク ドメインのハッシュです。 AD 環境 (オンプレミス) の SID は、ネットワーク エイリアスのハッシュであり、プロバイダーを識別します。

まだログインできず、"現在の資格情報でログインする権限がありません" というエラー メッセージが表示されている場合。 数秒すると、ログイン ページにリダイレクトされます。このトピックの [ADFS](#ADFS) のセクションを参照してください。

## <a name="systemdatasqlclientsqlexception-0x80131904-and-systemcomponentmodelwin32exception-0x80004005"></a>System.Data.SqlClient.SqlException (0x80131904) および System.ComponentModel.Win32Exception (0x80004005)
次のエラーのいずれかが表示された場合:

- System.Data.SqlClient.SqlException (0x80131904): 接続がサーバーで正常に確立されましたが、ログイン プロセス時にエラーが発生しました。 (プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは、信頼されていない機関によって発行されました。)
- System.ComponentModel.Win32Exception (0x80004005): 証明書チェーンは、信頼されていない機関によって発行されました

証明書がインストールされていないか、正しいユーザーにアクセス権が与えられていません。 このエラーを解決するには、公開キー SQL サーバー証明書をすべての Service Fabric ノードに追加します。

## <a name="keyset-doesnt-exist"></a>Keyset が存在しません
キーセットが存在しないことを検索する場合は、すべてのコンピューターでスクリプトが実行されなかったことを意味します。 環境の VM の設定を確認および完了します。
- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#setupvms)
- [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupvms)

各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。

また正しいドメインを使用していることを確認する .csv ファイルを確認します。

## <a name="error-runasync-failed-due-to-an-unhandled-fabricexception-causing-replica-to-fault"></a>エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」
「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException:」というこのエラーが発生した場合は、最初の織物アップグレードでは、コード バージョンと設定バージョンの両方を指定する必要があります。 要求された値: 0.0.0.0:"。ClusterConfig.json 診断を変更します。ネットワーク共有からローカル パスに保存します。`\\server\path` から既定値の `C:\ProgramData\SF\DiagnosticsStore` など。

## <a name="error-dbsync-db-sync-issues"></a>エラー、Dbsync (DB 同期) の問題
データベースの同期の問題が発生した場合、AOS の作業ディレクトリ、ex `C:\ProgramData\SF\AOS1\Fabric\work\Applications\AXSFType_App8\log` を参照し、すべての AOS コンピューターで次の確認を実行します。

- **イベント ビューアー** > **カスタム ビュー** > **管理イベント**
- **イベント ビューアー** > **アプリケーションおよびサービス ログ** > **Microsoft** > **Dynamics** > **AX-DatabaseSynchronize**

## <a name="service-fabric-aos-node-error-during-build-execution-timeout-expired"></a>ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ
エラー メッセージ:

```
The timeout period elapsed prior to completion of the operation or the server is not responding.
The statement has been terminated.
```

一度に 1 つの AOS マシンのみ DB Sync できます。 これは、AOS VM の 1 つが DB Sync を実行していて、他が警告を出すことができないために、このエラー メッセージは無視しても問題ありません。 DB の同期が実行されているという事実は、警告を発していない AOS VM の **イベント ビューアー** > **アプリケーションとサービス ログ** > **Microsoft** > **Dynamics** > **AX-DatabaseSynchronize/Operational** の順に確認して検証できます。

## <a name="error-requirenonce-is-true-default-but-validationcontextnonce-is-null"></a>エラー、「RequireNonce が True (既定) ですが、validationContext.Nonce は Null です」
AX にログイン後 Internet Explorer で HTTP エラー 500 としても表示されます。 Internet Explorer がセキュリティ強化の構成になっている場合、発行された nonce は検証できません。

AX にログインするには、サーバー マネージャーを使用して Internet Explorer のセキュリティ強化設定を無効にします。

## <a name="error-invalid-algorithm-specified--cryptography"></a>エラー、「無効なアルゴリズムが指定されている/暗号化」
このエラーが発生した場合は、Microsoft Enhanced RSA および AES Cryptographic Provider を使用する必要があります。 詳細については、証明書の要求を確認します。 また、credentials.json ファイルの構造が正しいことを確認します。

正しいプロバイダーを使用して証明書を再作成する必要がある場合は、次の手順に従います。

1. 正しいプロバイダーを使用して証明書を再度作成します。
1. ConfigTemplate.xml の変更
1. クラスター内のすべてのコンピューターでインフラストラクチャ スクリプトを実行し、Test-D365FOConfiguration.ps1 スクリプトに合格するかどうかを確認します。
1. LCS から環境を再構成します。

## <a name="error-partition-is-below-target-replica-or-instance-count"></a>エラー、「パーティションがターゲット レプリカまたはインスタンス数を下回っています」
これはルート エラーではありません。 このエラーは、各ノードのステータスが準備できていないことを意味します。 AXSF/AOS で、ステータスがまだ inBuild である可能性があります。
イベント ビューアーに移動してルート エラーを取得します。

## <a name="error-unable-to-find-certificate-when-running-test-d365foconfigurationps1"></a>エラー、「証明書を検出できません」 Test-D365FOConfiguration.ps1 を実行した場合
このエラーが表示された場合は、証明書/拇印が複数の目的で結合されているかどうかを確認してください。 たとえば、クライアントおよび SessionAuthentication が結合される場合、このエラーが発生します。 証明書を結合しないことをお勧めします。 詳細については、「証明書の要件および domain.com\user 対 domain\user (ex の acl.csv を確認する」を参照してください。 NETBIOS 構造体)。

## <a name="client-and-server-cant-communicate-because-they-do-not-have-a-common-algorithm"></a>クライアントとサーバーは共通のアルゴリズムを持たないため通信できません
これが発生した場合、作成された証明書で、手順 2 で説明されているように指定されたプロバイダーが使用されていることを確認します。 環境の証明書を計画し、取得します。 
- [プラットフォーム update 12](setup-deploy-on-premises-pu12.md#plancert)
- [プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#plancert)

## <a name="find-a-list-of-group-managed-service-accounts-gmsa"></a>グループ管理サービス アカウント (gMSA) の一覧を検索します
すべてのグループとホストの一覧を検索するには、`Get-ADServiceAccount -Identity svc-LocalAgent$ -Properties PrincipalsAllowedToRetrieveManagedPassword` を参照してください。

## <a name="addcerttoserviceprincipal-script-failing-on-import-module"></a>Import-Module での AddCertToServicePrincipal スクリプトの失敗
Import-Module での AddCertToServicePrincipal スクリプトの失敗: ファイルまたはアセンブリ 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' またはその依存関係のうちのいずれか 1 つを読み込めませんでした。 厳密な名前の検証に失敗しました。 (HRESULT からの例外: 0x8013141A) には、同じモジュールの複数のバージョンがインストールされている場合があります。

この問題を解決するには、PowerShell で次のコマンドを実行します。

```powershell
Uninstall-Module -Name AzureRM
Install-Module AzureRM
```

PowerShell ウィンドウを閉じて、もう一度やり直してください。

## <a name="reportingservicessetupexe-error"></a>ReportingServicesSetup.exe エラー
ReportingServicesSetup.exe エラー: 0 : アプリケーション ファブリック:/10 分後、ReportingService は OK ではありません。アプリケーション: ReportingServicesBootstrapper.exe フレームワーク バージョン v4.0.30319 説明: 未処理の例外により、プロセスが中止されました。

このエラーが発生した場合、厳密な名前検証はレポート サーバーで有効化されます。 これを解決するには、レポート サーバー マシンで config-PreReq スクリプトを実行します。

## <a name="requested-operation-requires-elevation"></a>要求された操作には、昇格が必要です
AOS ユーザーは、ローカル管理者グループに属しておらず、UAC は、正しく無効化されていません。 この問題を解決するには、次の手順を実行します。
1. 「VM のドメインへの参加」のセクションで説明されているように、ローカル管理者として AOS ユーザーを追加します。
2. すべての AOS コンピューターで、Config-PreReq スクリプトを実行します。
3. テスト構成スクリプトがパスすることを確認します。
4. UAC が変更された場合は、有効にするマシンを再起動する必要があります。

## <a name="files-in-use-errors"></a>使用中ファイルのエラー
Service Fabric により指示された除外ルールを設定します。 詳細については、「[Service Fabric のスタンドアロン クラスター展開の計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)」を参照してください。

## <a name="apply-deployable-packages-during-deployment"></a>配置中に配置可能パッケージを適用する
### <a name="package-deployment-fails-due-to-path-too-long-exception"></a>「パスが長過ぎる」例外によってパッケージの展開が失敗する
Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。 文字数の制限を超過した場合、次のエラーが表示されます。

**System.IO.PathTooLongException: 指定したファイル パス、ファイル名、またはその両方が長すぎます。System.IO.PathHelper.GetFullPathName では、完全修飾ファイル名は 260 文字未満で、ディレクトリ名は 248 文字未満でなければなりません。**

このエラーを回避するには、パッケージ名を短くしてパッケージを再度適用するか、オンプレミス資産の共有パスの全長を短くします。

### <a name="package-deployment-fails-because-of-serialization-error"></a>シリアル化エラーが原因でがパッケージの展開に失敗する
パッケージの配置中に、**シリアル化バージョンの不一致が検出。ランタイム DLLs が配置されたメタデータと同期していることを確認してください。ファイル「XXX」のバージョン。DLL 「XXX」のバージョン**というエラーが発生した場合、パッケージが配置されている環境とは異なるバージョンの環境でパッケージが開発された可能性があります。
この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。 パッケージのアップロード先にあるアセット ライブラリの **追加の詳細** セクションをクリックすることにより、パッケージ バージョンを確認することができます。 エラーを修正するには、オンプレミス環境に展開されたバージョンと同じバージョンまたはそれ以前のバージョンにパッケージを生成します。

### <a name="package-deployment-fails-because-of-dependencies-on-missing-modules"></a>欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する
依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次と類似するメッセージが表示されます。

**パッケージ [dynamicsax-My\_commonextension.7.0.4679.35176.nupkg に依存関係がありません: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor]]**

**パッケージ [dynamicsax-My\_coreextension.7.0.4679.35176.nupkg に依存関係がありません: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor]]**

**パッケージ [dynamicsax-My\_uiextension.7.0.4679.35176.nupkg に依存関係がありません: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests]]**

問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーにログインし、アプリケーションとサービスを開き、**Microsoft** > **Dynamics** > **AX SetupModuleEvents** に移動します。 これにより、モジュールがないイベントが表示されます。 たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor モジュールです。
この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。 依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。 モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除します。 詳細については、「[モデルのエクスポートとインポート](../dev-tools/models-export-import.md)」を参照してください。

### <a name="package-deployment-works-on-one-box-environment-but-not-in-the-sandbox-environment"></a>パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない
1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、サンドボックスには実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。 パッケージを開発環境で構築が1つのシステムで環境に格納されているモジュールにこの依存関係いないサンド ボックス環境で、パッケージでは動作しませんサンド ボックス環境場合。
この問題を解決するには、依存するすべてのモジュールを確認し、実稼動環境で不要なファーム アダプターまたはその他のモジュールをプルしないようにします。 ビルド ボックスからパッケージを取得することをお勧めします。

