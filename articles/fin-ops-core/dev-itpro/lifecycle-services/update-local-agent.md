---
title: ローカル エージェントの更新
description: このトピックでは、ローカル エージェントを更新する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2017-12-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 11c171ef25e086a1b1b8b6fe34b8fcfaafa4d9ab
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811693"
---
# <a name="update-the-local-agent"></a>ローカル エージェントの更新

[!include [banner](../includes/banner.md)]

このトピックでは、ローカル エージェントを更新する方法について説明します。 ローカル エージェントの最新バージョンはバージョン 2.3.1 で、2019 年 9 月にリリースされました。

| ローカル エージェントのバージョン | 能力 | 
|---------------------|------------|
| Null                | この初期バージョンでは、Platform update 8 が導入されています。 |
| 1.0.0               | このバージョンでは、展開が失敗した場合のために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になります。 |
| 1.1.0               | このバージョンでは、正常に展開するために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になり、複数モデルのパッケージ展開が可能になり、プラットフォーム更新プログラム 8 および 11 が展開されます。 | 
| 2.0.0               | このバージョンでは、サービス フローが可能になり、プラットフォーム更新プログラム 12 が展開されます。 |
| 2.1.0               | このバージョンでは、**準備**および**更新**が 2 つの個別のステップである 2 段階サービスが可能になります。 |
| 2.1.1               | このバージョンはダウンロードが失敗したときに発生する LCS 管理ボタンが利用できない問題を修正します。 その他の変更には、Azure Storage との通信を改善し TLS 1.2 を有効にする Azure Storage ライブラリの更新を含みます。  |
| 2.1.2               | このバージョンには、更新されたAzure依存関係が含まれており、ダウンロードの安定性を向上し、ファイルがダウンロードされた場合に正しく評価するロジックを使用 これにより、ファイルが完全にダウンロードされるという問題が修正されますが、論理上数バイトが不足していると見なされ、ダウンロードに失敗します。  |
| 2.2.0               | このバージョンは、クリーンアップ中にロックされた dll を修正し、Office 365 にも使用される ADFS をサポートするための前提条件を有効にします。 |
| 2.3.0               | このバージョンに、配置前スクリプトと配置後スクリプトのサポートが追加されます。  |
| 2.3.1               | このバージョンでは、一部の環境でのクリーンアップ中に発生する可能性があるオーケストレーション サービスのクラッシュを修正します。<br><br>プラットフォーム更新プログラム 29 以前のバージョン 10.0.5 を配置するには、FinancialReportingDeployer.exe.config の自動更新に対する配置前スクリプトの使用が必要になります。それは [オンプレミス配置のトラブルシューティング](../../dev-itpro/deployment/troubleshoot-on-prem.md#FREntityFramework) で検索できます。 |

## <a name="whats-new-in-local-agent-230"></a>Local agent 2.3.0 の新機能

- ローカル エージェント 2.3.0 は、カスタム実行を有効にします [配置前および配置後のスクリプト](../../dev-itpro/lifecycle-services/pre-post-scripts.md)。
- これは、古いプラットフォーム更新プログラムの展開に関して 2.2.0 で採用された問題を修正します。
- このリリースでは、監視エージェントを削除して LBDTelemetry という新しいサービスを導入し、これを ETWManifests のインストールの際に使用します。

> [!IMPORTANT]
> このリリースでは、LCS から新しいローカル エージェント構成ファイルをダウンロードする必要があります。 問題が発生した場合は、[オンプレミス配置のトラブルシューティング](../../dev-itpro/deployment/troubleshoot-on-prem.md) を参照してください。 

## <a name="whats-new-in-local-agent-210"></a>Local agent 2.1.0 の新機能
- ローカル エージェント 2.1.0 では、**環境の準備**および**環境の更新**が 2 つの異なる手順および明示的アクションである 2 フェーズのサービスを有効にします。 事前準備を行い、ユーザーが準備中に環境を使用できるようにし、実際の更新環境アクションが発生する際にダウンタイムを通知することで、オンプレミス環境に更新プログラムを適用する場合に顧客が取る必要があるダウンタイムの合計が削減されます。

## <a name="whats-new-in-local-agent-200"></a>Local agent 2.0.0 の新機能
- ローカル エージェント 2.0.0 はプラットフォーム更新プログラム 12 を展開できます。
- プラットフォーム更新 12 の配置の初回成功まで、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は有効になります。
- プラットフォーム更新 12 の配置の初回成功時は、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は無効になります。 配置が成功した後、定期的な更新エクスペリエンスを使用して環境を更新することができます。

> [!NOTE]
> ローカル エージェント 2.0.0 は、プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11 を展開**できません**。 プラットフォーム更新プログラムを展開するには、バージョン 1.1.0 が必要です。

## <a name="download-the-latest-local-agent-and-configuration-from-lcs"></a>LCS から最新のローカル エージェントおよびコンフィギュレーションをダウンロード

> [!NOTE]
> 現在の配置では、ローカル エージェントの以前のバージョンを要求する場合は、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリからそれをダウンロードします。 ローカル エージェント バージョン v1.1.0 をダウンロードするには、**共用資産ライブラリ - >モデル**に移動し、Dynamics 365 for Finance and Operations オンプレミス - ローカル エージェント v1.1.0** をクリックします。

> プラットフォーム更新プログラム 12 の展開および更新プログラム フローの完成には、バージョン 2.0.0 かそれ以降のバージョンが必要です。

1. LCS で、**プロジェクト設定** > **オンプレミス コネクタ**を選択します。
2. 環境へのコネクタを選択し、**編集** を選択します。
3. ページの左側にあるメニューの、**ホスト インフラストラクチャ設定**を選択し、**エージェント インストーラーのダウンロード**を選択します。

    この時点で、zip ファイルがダウンロードされ、かつブロックされていないことを確認する必要があります。

4. zip ファイルに移動し、右クリックして **プロパティ** を選択します。
5. **プロパティ** ダイアログ ボックスで、**ブロック解除**を選択してから**適用**を選択します。
6. **エージェントのコンフィギュレーション**タブで、**コンフィギュレーションのダウンロード**を選択し、localagent-config.json コンフィギュレーション ファイルをダウンロードします。

## <a name="update-the-local-agent"></a>ローカル エージェントの更新

1. ZIP ファイルと localagent-config.json ファイルを、**Orch1** 仮想マシン (VM) の **c:\\DynamicsAgent** などの、**Orchestrator** ノードの 1 つにコピーします。
2. エージェント インストーラを C:\\DynamicsAgent\\LocalAgent に解凍します。
3. localagent-config.json ファイルを \\DynamicsAgent\\LocalAgent にコピーします。
4. **コマンド プロンプト** ウィンドウで、C:\\DynamicsAgent\\LocalAgent に移動して、次のコマンドを実行します。

    ```
    LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

    > [!NOTE]
    > エージェントをクリーンアップするには、現在のエージェントのバイナリ ファイルを使用する必要があります。 現在のエージェントのバイナリ ファイルがない場合は、Service Fabric Explorer からローカル エージェント アプリケーションを削除できます。

5. クリーンアップ操作を終了するには、任意のキーを押します。
6. Service Fabric Explorer を調べ、**Orchestrator** ノードの **展開済みアプリケーション** セクションにアプリケーションがないことを確めて、ローカル エージェントが正常にクリーンアップされことを確認します。
7. ローカル エージェントが正常にクリーンアップされた後は、次のコマンドを実行します。

    ```
    LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

8. ローカル エージェントが正常にインストールされてから、LCS のオンプレミス コネクタに戻るようにします。
9. **設定の検証**タブで、**メッセージ エージェント**を選択して、新しいローカル エージェントへの LCS 接続をテストします。
