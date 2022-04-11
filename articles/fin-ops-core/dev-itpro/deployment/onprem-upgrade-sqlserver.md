---
title: Microsoft Dynamics 365 Finance + Operations (on-premises) 環境の SQL Server インスタンスのアップグレードまたは置換
description: このトピックでは、環境で使用している Microsoft SQL Server インスタンスまたはクラスターをアップグレードする方法について説明します。
author: faix
ms.date: 12/14/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3123d5fdc61fb3f5561b6ff7b7f38670295db570
ms.sourcegitcommit: 3cb1f49a02e4a849fc34ffeb81fe507f0608b35e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2022
ms.locfileid: "8464859"
---
# <a name="upgrade-or-replace-the-sql-server-instance-of-microsoft-dynamics-365-finance--operations-on-premises-environments"></a>Microsoft Dynamics 365 Finance + Operations (on-premises) 環境の SQL Server インスタンスのアップグレードまたは置換

このトピックでは、環境で使用している Microsoft SQL Server インスタンスまたはクラスターをアップグレードする方法について説明します。 SQL Server メジャー バージョンから別のバージョンにアップグレードしますが、[インプレース アップグレード](/sql/database-engine/install-windows/choose-a-database-engine-upgrade-method) をしない場合は、このプロセスを完了する必要があります。 インプレース アップグレードを実行する場合でも、手順の一部は適用されませんが、このトピックのガイダンスに従ってください。

## <a name="prerequisites-for-upgrading-the-sql-server-version"></a>SQL Server バージョンをアップグレードするための前提条件

### <a name="upgrade-from-sql-server-2016-to-sql-server-2019"></a>SQL Server 2016 から SQL Server 2019 へのアップグレード

- この環境は、アプリケーション バージョン 10.0.21 以降である必要があります。
- このローカル エージェントは、バージョン 2.7.0 以降である必要があります。

## <a name="preparation"></a>準備

1. 新しい SQL Server インスタンスを仮想マシン (VM) に配置するか、新しい SQL クラスターを作成します。
1. [SQL Server の設定](./setup-deploy-on-premises-pu41.md#setupsql) の説明に従って、新しいインスタンスまたはクラスターを構成します。
1. 自己署名証明書を使用する場合、これらの証明書が、Azure Service Fabric Cluster内の Application Object Server (AOS)、Management Reporter (MR)、および Orchestrator ノードにインポート済みであることを確認します。

## <a name="database-operations"></a>データベース操作

1. ダウンタイムが始まるため、ユーザーが接続していないことを確認してください。
1. 現在の SQL Server インスタンスまたはクラスターからすべてのデータベースをバックアップします。
1. データベース バックアップを新しい SQL Server インスタンスまたはクラスターに復元します。
1. データベースを復元した後に、[データベースの構成](./setup-deploy-on-premises-pu41.md#configuredb) でスクリプトを実行します。

## <a name="upgrade-other-sql-server-components"></a>他の SQL Server コンポーネントのアップグレード

環境間の SQL Server コンポーネントは、同じバージョンである必要があります。 たとえば、SQL Server 2019 にアップグレードする場合、SQL Server Reporting Services (SSRS)、SQL Server Integration Services (SSIS)、データベース エンジンは、すべて同じバージョンである必要があります。

1. AOS ノードで、SSIS コンポーネントをアップグレードします。
1. Business Intelligence (BI) ノードで、SSRS とデータベース エンジン コンポーネントをアップグレードします。

## <a name="update-the-local-agent"></a>ローカル エージェントの更新

1. Orchestrator ノードから次のコマンドを実行して、ローカル エージェントをクリーンアップします。

    ```powershell
    LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

1. [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) で、SQL Server インスタンスまたはクラスターの新しい完全修飾ドメイン名 (FQDN) でコネクタ構成を更新します。

    ![コネクタ データベースの設定を更新します。](media/ConnectorSettingsDB.png)

1. 新しい構成ファイルをダウンロードします。
1. 構成ファイルで、SQL Server バージョンを更新します。 指定するバージョンは、環境内に存在する SQL Server のバージョンと一致している必要があります。 詳細については、[ローカル エージェントの配置コンフィギュレーション](./onprem-localagent-options.md) を参照してください。

    ```json
    "deploymentOptions": {
        ...
        "sqlServerVersion" : {
            "value": "2019"
        },
        ...
    }
    ```

1. 新しい構成ファイルでローカル エージェントをインストールします。

    ```powershell
    LocalAgentCLI.exe Install <path of the new localagent-config.json>
    ```

## <a name="force-the-re-adding-of-the-assemblies-to-the-global-assembly-cache"></a>アセンブリの再追加をグローバル アセンブリ キャッシュに強制する

通常、パッケージ配置で環境をサービスする場合、AXSFType の Service Fabric パッケージ バージョンが変更します。 これにより、環境に対して、追加の配置やサービス操作が実行されます。 **更新設定** アクションを使用しても、バージョンは変更されません。 その結果、適切なアセンブリがグローバル アセンブリ キャッシュにありません。 アセンブリの再追加をグローバル アセンブリ キャッシュに強制するには、次の手順を実行します。

1. aos-storage ファイル共有に移動します。
2. **GacAssemblies** フォルダーを開きます。
3. AOS ノードの名前に対応するフォルダーの一覧が表示されます。 いずれかのフォルダーを開きます。 
4. 既存の .txt ファイルの名前を1.0.txt に変更します。
5. 各フォルダーについて、ステップ 4 を繰り返します。

## <a name="update-your-environment-settings"></a>環境設定の更新

1. [LCS](https://lcs.dynamics.com) で、SQL Server の更新を希望する環境についての **完全な詳細情報** リンクを選択します。
1. **管理** を選択し、**更新の設定** を選択します。
1. 設定を更新する場合は、新しい SQL Server インスタンスまたはクラスターの FQDN を更新します。

    ![環境データベースの設定を更新します。](media/EnvironmentSettingsDB.png)

1. **準備** を選択します。

    ダウンロードおよび準備が完了すると、**環境の更新** ボタンが表示されます。

    ![環境の更新ボタン。](media/0a9d43044593450f1a828c0dd7698024.png)

1. **環境の更新** を選択して、環境の更新を開始します。

    この環境は、新しいバージョンの SQL Server と対話するように再配置され、構成されます。
