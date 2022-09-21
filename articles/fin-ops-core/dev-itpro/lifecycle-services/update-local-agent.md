---
title: ローカル エージェントの更新
description: この記事では、ローカル エージェントを更新する方法について説明します。
author: faix
ms.date: 09/02/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2017-12-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: ac4846df45c3b4362dcfb7c6428341a212c5012c
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403526"
---
# <a name="update-the-local-agent"></a>ローカル エージェントの更新

[!include [banner](../includes/banner.md)]

この記事では、ローカル エージェントを更新する方法について説明します。 ローカル エージェントの最新バージョンは、2022 年 6 月にリリースされたバージョン 3.1.0 です。

> [!IMPORTANT]
> 準備フェーズが完了した場合でも、サービス操作中にローカル エージェントを更新しないでください。 

| ローカル エージェントのバージョン | 能力 | 
|---------------------|------------|
| 3.1.0               | このバージョンでは、Service Fabric SDK をアップグレードし、新しい展開オプションを追加します。 |
| 3.0.0               | このバージョンには、Edge Scale Unit アプリケーション ライフサイクル管理のサポートが含まれています。 |
| 2.7.2               | このバージョンには、古いアプリケーション バージョンを配置するための修正が含まれています。 | 
| 2.7.1               | このバージョンでは、新しい展開オプションが導入され、展開オプションによるバグが修正されます。 |
| 2.7.0               | 10.0.21 以降のバージョンへの展開または更新を有効にします。 さらに、このバージョンでは Microsoft SQL Server 2019 と一部のバグ修正プログラムがある環境への配置が有効になります。 |
| 2.6.0               | このバージョンは、Service Fabric SDK をアップグレードし、更新状態のバグを修正して、アプリケーション プロビジョニングのタイムアウトを増やします。 |
| 2.5.0               | このバージョンは依存関係を更新し、クリーンアップ バグを修正します。 |
| 2.4.0               | このバージョンでは、展開の問題が修正され、ローカル エージェントのランタイムがアップグレードされます。 |
| 2.3.1               | このバージョンでは、一部の環境でのクリーンアップ中に発生する可能性があるオーケストレーション サービスのクラッシュを修正します。<br><br>プラットフォーム更新プログラム 29 以前のバージョン 10.0.5 を展開するには、FinancialReportingDeployer.exe.config. の自動更新に事前配置スクリプトを使用する必要があります。詳細については、[オンプレミス展開のトラブルシューティング](../../dev-itpro/deployment/troubleshoot-on-prem.md#FREntityFramework)を参照してください。 |
| 2.3.0               | このバージョンに、配置前スクリプトと配置後スクリプトのサポートが追加されます。  |
| 2.2.0               | このバージョンでは、クリーンアップ中にロックされた dll を修正し、Microsoft 365 でも使用される Active Directory フェデレーション サービス (AD FS) をサポートするための前提条件を有効にします。 |
| 2.1.2               | このバージョンには、更新されたAzure依存関係が含まれており、ダウンロードの安定性を向上し、ファイルがダウンロードされた場合に正しく評価するロジックを使用 これにより、ファイルが完全にダウンロードされるという問題が修正されますが、論理上数バイトが不足していると見なされ、ダウンロードに失敗します。  |
| 2.1.1               | このバージョンはダウンロードが失敗したときに発生する Lifecycle Services (LCS) **管理** ボタンが利用できない問題を修正します。 その他の変更には、Azure Storage との通信を改善し TLS 1.2 を有効にする Azure Storage ライブラリの更新を含みます。  |
| 2.1.0               | このバージョンでは、**準備** および **更新** が 2 つの個別のステップである 2 段階サービスが可能になります。 |
| 2.0.0               | このバージョンでは、サービス フローが可能になり、プラットフォーム更新プログラム 12 が展開されます。 |
| 1.1.0               | このバージョンでは、正常に展開するために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になり、複数モデルのパッケージ展開が可能になり、プラットフォーム更新プログラム 8 および 11 が展開されます。 | 
| 1.0.0               | このバージョンでは、展開が失敗した場合のために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になります。 |
| Null                | この初期バージョンでは、Platform update 8 が導入されています。 |

## <a name="whats-new-in-local-agent-310"></a>ローカル エージェント 3.1.0 の新機能

- ローカル エージェント 3.1.0 は、新しい Service Fabric SDK とランタイムを取得します。
- このリリースでは、新しい展開オプションが導入され、[環境が Regression Suite Automation Tool (RSAT) で機能するよう構成する必要があると指定する](../../dev-itpro/deployment/onprem-localagent-options.md#specify-that-an-environment-should-be-configured-to-work-with-the-regression-suite-automation-tool)ことができます。

> [!IMPORTANT]
> このリリースは、8.1+ Service Fabric クラスターとのみ互換性があります。

## <a name="whats-new-in-local-agent-300"></a>ローカル エージェント 3.0.0 の新機能

- ローカル エージェント 3.0.0 には、スケール ユニット管理ポータルを通じて Edge Scale Unit のライフサイクルを管理するためのサポートが含まれます。 詳細については、[分散ハイブリッド トポロジ](../../../supply-chain/cloud-edge/cloud-edge-landing-page.md)を参照してください。
- このリリースでは、LCS から最新の変更を取り込むために .NET Framework バージョン 4.8 が必要です。

## <a name="whats-new-in-local-agent-272"></a>ローカル エージェント 2.7.2 の新機能

- Local agent 2.7.2 では、古いバージョンのアプリケーションの環境が配置に失敗する問題が修正されます。

## <a name="whats-new-in-local-agent-271"></a>ローカル エージェント 2.7.1 の新機能

- ローカル エージェント 2.7.1では、新しい展開オプションが[証明書の証明書失効リストのチェックをスキップするように指定する](../../dev-itpro/deployment/onprem-localagent-options.md#specify-that-checking-the-certificate-revocation-list-of-a-certificate-should-be-skipped)に導入されます。
- このリリースでは、**office365AdfsCompatibility** deploymentOption が正しく設定されなかった場合のバグに対処します。

## <a name="whats-new-in-local-agent-270"></a>ローカル エージェント 2.7.0 の新機能

- Local agent 2.7.0 は、10.0.21 以降のリリースを展開または更新する前提条件となるものです。 
- このリリースを使用すると、環境に固有の配置オプションに対する、限定された一連の配置オプションを指定できます。 特に、このリリースでは Microsoft SQL Server 2019 を使用する環境への配置が可能になります。 すべての有効なコンフィギュレーションについては、[ローカル エージェントの配置コンフィギュレーション](../../dev-itpro/deployment/onprem-localagent-options.md)を参照してください。
- さらに、このリリースは、ローカル エージェントが実行する gMSA アカウントが、一部の証明書のプライベート キーへのアクセス許可を失う問題に対処します。
- イベント ビューアーが開いている場合でも、LBDTelemetry-Agent アプリケーションを正常に開始できます。 

> [!IMPORTANT]
> このリリースは、10.0.21 以降のリリースを配置または更新するために **使用する必要があります**。
> このリリースでは、LCS から新しいローカル エージェント構成ファイルをダウンロードする必要があります。 問題が発生した場合は、[オンプレミス配置のトラブルシューティング](../../dev-itpro/deployment/troubleshoot-on-prem.md)を参照してください。 

## <a name="whats-new-in-local-agent-260"></a>ローカル エージェント 2.6.0 の新機能

- ローカル エージェント 2.6.0 は、新しい Service Fabric SDK とランタイムを取得します。
- このリリースでは、環境がダウンロード フェーズでスタックしているときに更新状態がトリガーされた場合、環境を更新せずに、環境が自動的に配置済みに移行するというバグが修正されています。 この場合、更新状態は、ダウンロード フェーズを失敗としてマークします。
- アプリケーションのプロビジョニングのタイムアウトが増加しました。

> [!IMPORTANT]
> このリリースは、7.x Service Fabric クラスターとのみ互換性があります。

## <a name="whats-new-in-local-agent-250"></a>ローカル エージェント 2.5.0 の新機能

- ローカル エージェント 2.5.0 は、さまざまな依存関係の新しいバージョンを取得します。 主な変更点は、Service Fabric と Entity Framework です。
- また、このリリースでは、サービスをクリーンアップせずにクリーンアップが失敗した場合、その後の再実行が常にクリーンアップ中に失敗するバグを修正します。

## <a name="whats-new-in-local-agent-240"></a>ローカル エージェント 2.4.0 の新機能

- ローカル エージェント 2.4.0 では、LCS から最新の変更を取り込むために .NET Framework バージョン 4.7.2 が必要になりました。 最新の要件を満たすために、LCS で利用可能な最新のインフラストラクチャ スクリプトを実行してください。
- このリリースでは、ハードコーディングされたタイムアウトのために AXService の展開が遅い環境で失敗する問題も修正されています。

## <a name="whats-new-in-local-agent-230"></a>ローカル エージェント 2.3.0 の新機能

- ローカル エージェント 2.3.0 は、カスタム実行を有効にします [配置前および配置後のスクリプト](../../dev-itpro/lifecycle-services/pre-post-scripts.md)。
- これは、古いプラットフォーム更新プログラムの展開に関して 2.2.0 で採用された問題を修正します。
- このリリースでは、監視エージェントを削除して LBDTelemetry という新しいサービスを導入し、これを ETWManifests のインストールの際に使用します。

> [!IMPORTANT]
> このリリースでは、LCS から新しいローカル エージェント構成ファイルをダウンロードする必要があります。 問題が発生した場合は、[オンプレミス配置のトラブルシューティング](../../dev-itpro/deployment/troubleshoot-on-prem.md)の記事を参照してください。 

## <a name="whats-new-in-local-agent-210"></a>ローカル エージェント 2.1.0 の新機能
- ローカル エージェント 2.1.0 では、**環境の準備** および **環境の更新** が 2 つの異なる手順および明示的アクションである 2 フェーズのサービスを有効にします。 事前準備を行い、ユーザーが準備中に環境を使用できるようにし、実際の更新環境アクションが発生する際にダウンタイムを通知することで、オンプレミス環境に更新プログラムを適用する場合に顧客が取る必要があるダウンタイムの合計が削減されます。

## <a name="whats-new-in-local-agent-200"></a>ローカル エージェント 2.0.0 の新機能
- ローカル エージェント 2.0.0 はプラットフォーム更新プログラム 12 を展開できます。
- プラットフォーム更新 12 の配置の初回成功まで、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は有効になります。
- プラットフォーム更新 12 の配置の初回成功時は、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は無効になります。 配置が成功した後、定期的な更新エクスペリエンスを使用して環境を更新することができます。

> [!NOTE]
> ローカル エージェント 2.0.0 は、プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11 を展開 **できません**。 プラットフォーム更新プログラムを展開するには、バージョン 1.1.0 が必要です。

## <a name="download-the-latest-local-agent-and-configuration-from-lcs"></a>LCS から最新のローカル エージェントおよびコンフィギュレーションをダウンロード

> [!NOTE]
> 現在の配置では、ローカル エージェントの以前のバージョンを要求する場合は、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリからそれをダウンロードします。 ローカル エージェント バージョン 1.1.0 をダウンロードするには、**共用資産ライブラリ -> モデル** に移動し、Dynamics 365 財務と運用 (オンプレミス) - ローカル エージェント v1.1.0** をクリックします。
>
> プラットフォーム更新プログラム 12 の展開および更新プログラム フローの完成には、バージョン 2.0.0 かそれ以降のバージョンが必要です。

1. LCS で、**プロジェクト設定** > **オンプレミス コネクタ** を選択します。
2. 環境へのコネクタを選択し、**編集** を選択します。
3. ページの左側にあるメニューの、**ホスト インフラストラクチャ設定** を選択し、**エージェント インストーラーのダウンロード** を選択します。

    この時点で、zip ファイルがダウンロードされ、かつブロックされていないことを確認する必要があります。

4. zip ファイルに移動し、右クリックして **プロパティ** を選択します。
5. **プロパティ** ダイアログ ボックスで、**ブロック解除** を選択してから **適用** を選択します。
6. **エージェントのコンフィギュレーション** タブで、**コンフィギュレーションのダウンロード** を選択し、localagent-config.json コンフィギュレーション ファイルをダウンロードします。

## <a name="update-the-local-agent"></a>ローカル エージェントの更新

1. ZIP ファイルと localagent-config.json ファイルを、**Orch1** 仮想マシン (VM) の **c:\\DynamicsAgent** などの、**Orchestrator** ノードの 1 つにコピーします。
2. エージェント インストーラを C:\\DynamicsAgent\\LocalAgent に解凍します。
3. localagent-config.json ファイルを \\DynamicsAgent\\LocalAgent にコピーします。
4. **コマンド プロンプト** ウィンドウで、C:\\DynamicsAgent\\LocalAgent に移動して、次のコマンドを実行します。

    ```Console
    LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

    > [!NOTE]
    > エージェントをクリーンアップするには、現在のエージェントのバイナリ ファイルを使用する必要があります。 現在のエージェントのバイナリ ファイルがない場合は、Service Fabric Explorer からローカル エージェント アプリケーションを削除できます。

5. クリーンアップ操作を終了するには、任意のキーを押します。
6. Service Fabric Explorer を調べ、**Orchestrator** ノードの **展開済みアプリケーション** セクションにアプリケーションがないことを確めて、ローカル エージェントが正常にクリーンアップされことを確認します。
7. ローカル エージェントが正常にクリーンアップされた後は、次のコマンドを実行します。

    ```Console
    LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

8. ローカル エージェントが正常にインストールされてから、LCS のオンプレミス コネクタに戻るようにします。
9. **設定の検証** タブで、**メッセージ エージェント** を選択して、新しいローカル エージェントへの LCS 接続をテストします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

