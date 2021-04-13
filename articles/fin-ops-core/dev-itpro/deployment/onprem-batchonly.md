---
title: オンプレミス配置でのバッチのみおよび対話型のみの AOS ノードのコンフィギュレーション
description: このトピックでは、環境をコンフィギュレーションして、バッチのみおよび対話型のみの AOS ノードを配置できるようにする方法について説明します。
author: faix
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 68599064707bb6c0258373fb215e544885e67941
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745329"
---
# <a name="configure-batch-only-and-interactive-only-aos-nodes-in-on-premises-deployments"></a>オンプレミス配置でのバッチのみおよび対話型のみの AOS ノードのコンフィギュレーション

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> この機能は、アプリケーション更新 10.0.12 (プラットフォーム更新 36) 以降でサポートされます。

このトピックでは、環境をコンフィギュレーションして、バッチのみおよび対話型のみの Application Object Server (AOS) ノードを配置できるようにする方法について説明します。

この機能を使用できるようにするために、Microsoft は 2 つの新しい Microsoft Azure Service Fabric ノード タイプを導入しました。 バッチ専用 AOS ノードの場合、新しいノード タイプは **BatchOnlyAOSNodeType** です。 対話型のみの AOS ノードの場合、新しいノード タイプは **InteractiveOnlyAOSNodeType** です。

> [!NOTE]
> 従来の配置オプションでは、AOS ノードが対話型でバッチ ジョブを実行している場合でもサポートされますが、これらの変更による影響はありません。

## <a name="sizing"></a>サイズ変更

サンドボックス環境では、各タイプのノードを 2 つ以上使用することをお勧めします。

運用環境では、それぞれのタイプのノードを 3 つ以上にする必要があります。

## <a name="new-deployments"></a>新しい配置

1. [オンプレミス環境の設定と配置](./setup-deploy-on-premises-pu12.md#describeconfig)で説明されているコンフィギュレーションを記述する場合は、**configtemplate.xml** ファイルを編集して新しいノード タイプを追加します。 完了すると、新しい **NodeType** セクションは次の例のようになります。

    ```xml
    <NodeType name="InteractiveOnlyAOSNodeType" primary="false" namePrefix="AOS" purpose="AOS">
        <VMList>
            <VM name="LBDE05FS1AOS01" ipAddress="192.168.5.51" faultDomain="fd:/fd0" updateDomain="ud0" />
            <VM name="LBDE05FS1AOS02" ipAddress="192.168.5.52" faultDomain="fd:/fd1" updateDomain="ud1" />
            <VM name="LBDE05FS1AOS03" ipAddress="192.168.5.53" faultDomain="fd:/fd0" updateDomain="ud2" />
        </VMList>
    </NodeType>
    <NodeType name="BatchOnlyAOSNodeType" primary="false" namePrefix="AOS" purpose="AOS">
        <VMList>
            <VM name="LBDE05FS1AOS04" ipAddress="192.168.5.54" faultDomain="fd:/fd0" updateDomain="ud0" />
            <VM name="LBDE05FS1AOS05" ipAddress="192.168.5.55" faultDomain="fd:/fd1" updateDomain="ud1" />
            <VM name="LBDE05FS1AOS06" ipAddress="192.168.5.56" faultDomain="fd:/fd0" updateDomain="ud2" />
        </VMList>
    </NodeType>
    ```

2. [オンプレミス環境の設定と配置](./setup-deploy-on-premises-pu12.md#describeconfig)の残りの指示に通常どおりに従います。

## <a name="existing-deployments"></a>既存の配置

1. コンフィギュレーション ファイルを保存する時点まで、[AOS ノードの削除](onprem-remove-reinstall-AOS-node.md#option-1-use-a-configuration-file-preferred-option)の手順に従います。

    > [!IMPORTANT]
    > オプション 1「構成ファイルを使用する (推奨オプション)」を使用する必要があります。 オプション 2 は使用 **しない** でください。

2. **ClusterConfig.json** ファイルの編集を続け、新しいノード タイプを **NodeTypes** セクションに追加します。 完了すると、**NodeTypes** セクションは次の例のようになります。

    ```json
    "NodeTypes": [
        {
            "Name": "AOSNodeType",
            "PlacementProperties": {
                "IsAosEnabled": "True"
            },
            "ClientConnectionEndpointPort": 19000,
            "HttpGatewayEndpointPort": 19080,
            "ReverseProxyEndpointPort": 19081,
            "LeaseDriverEndpointPort": 19002,
            "ClusterConnectionEndpointPort": 19001,
            "ServiceConnectionEndpointPort": 19003,
            "ApplicationPorts": {
                "StartPort": 20001,
                "EndPort": 20031
            },
            "IsPrimary": false
        },
        {
            "Name": "BatchOnlyAOSNodeType",
            "PlacementProperties": {
                "IsAosEnabled": "True"
            },
            "ClientConnectionEndpointPort": 19000,
            "HttpGatewayEndpointPort": 19080,
            "ReverseProxyEndpointPort": 19081,
            "LeaseDriverEndpointPort": 19002,
            "ClusterConnectionEndpointPort": 19001,
            "ServiceConnectionEndpointPort": 19003,
            "ApplicationPorts": {
                "StartPort": 20001,
                "EndPort": 20031
            },
            "IsPrimary": false
        },
        {
            "Name": "InteractiveOnlyAOSNodeType",
            "PlacementProperties": {
                "IsAosEnabled": "True"
            },
            "ClientConnectionEndpointPort": 19000,
            "HttpGatewayEndpointPort": 19080,
            "ReverseProxyEndpointPort": 19081,
            "LeaseDriverEndpointPort": 19002,
            "ClusterConnectionEndpointPort": 19001,
            "ServiceConnectionEndpointPort": 19003,
            "ApplicationPorts": {
                "StartPort": 20001,
                "EndPort": 20031
            },
            "IsPrimary": false
        },
        ...
    ]
    ```

3. クラスターからのノードの削除が完了するまで、停止したポイントから [AOS ノードの削除](onprem-remove-reinstall-AOS-node.md#option-1-use-a-configuration-file-preferred-option)の手順に引き続き従ってください。
4. Service Fabric Cluster から削除したコンピューターで、次の手順を実行します。

    1. Service Fabric データ ルート (**C:\\ProgramData\\SF**) と Service Fabric ログ ルート (**C:\\ProgramData\\SF\\Log**) の内容を削除します。
    2. Windows Server 用 Service Fabric のスタンドアロン パッケージをバーチャル マシン (VM) またはコンピューターにコピーまたはダウンロードします。
    3. パッケージを解凍します (**C:\\Temp\\ServiceFabricStandalone**)。
    4. Windows PowerShell を管理者として開きます。
    5. 次のコマンドを実行します。

        > [!IMPORTANT]
        > 使用しているコンピューター コンフィギュレーションのパラメーターを必要に応じて置き換えます。

        ```powershell
        cd C:\Temp\ServiceFabricStandalone
        .\AddNode.ps1 -NodeName AOS_12 -NodeType BatchOnlyAOSNodeType -NodeIpAddressOrFQDN 192.168.5.12 -ExistingClientConnectionEndpoint 192.168.5.21:19000 -UpgradeDomain ud0 -FaultDomain fd:/fd0 -X509Credential -ServerCertThumbprint 1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A -AcceptEULA -StoreLocation LocalMachine -StoreName MY -FindValueThumbprint 1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A
        ```

        > [!NOTE]
        > 最初にノードが Service Fabric Explorer に再表示されたときは、古いノード タイプが表示されている可能性があります。 ただし、数分後に更新されたノード タイプが表示されます。

5. **ClusterConfig.json** ファイルについて、Service Fabric Cluster を再度照会します。

    ```powershell
    Get-ServiceFabricClusterConfiguration -UseApiVersion -ApiVersion 10-2017 > C:\Temp\ClusterConfig.json
    ```

6. **fabricSettings** セクションで、**NodesToBeRemoved** パラメーターを削除します。 完了すると、**fabricSettings** セクションは次の例のようになります。

    ```json
    "fabricSettings": [
        {
            "name": "Setup",
            "parameters": [
                {
                    "name": "FabricDataRoot",
                    "value": "C:\\\\ProgramData\\\\SF"
                },
                {
                    "name": "FabricLogRoot",
                    "value": "C:\\\\ProgramData\\\\SF\\\\Log"
                }
            ]
        }
    ]
    ```

7. **セキュリティ** セクションから次の行を削除します。

    ```json
    "WindowsIdentities": {
        "\$id": "3"
    },
    ```

    > [!NOTE]
    > これらの行を削除しないと、後続の処理でで次のエラーメッセージが表示されます：
    >
    > *ValidationException: 認証タイプをセキュリティで保護されていないものから Windows に変更することはできません。*

8. 構成ファイルのバージョン番号をインクリメントします。 この変更は最小限の増分で行ってください。 次の例では、バージョン番号を **1.0.1** から **1.0.2** に変更しました。

    ```json
    "ClusterConfigurationVersion": "1.0.2"
    ```

9. 構成ファイルを保存します。
10. 管理者として Windows PowerShell を開き、次のコマンドを実行します。

    ```powershell
    Connect-ServiceFabricCluster
    Start-ServiceFabricClusterConfigurationUpgrade -ClusterConfigPath C:\Temp\ClusterConfig.json
    Update-ServiceFabricClusterUpgrade -UpgradeReplicaSetCheckTimeoutSec 30
    ```

11. アップグレードを監視するには、次のコマンドを実行します。

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

12. LCS からのアップグレードが完了したら、環境の更新をトリガーするために設定を変更しないで [設定の更新] ボタンを使用します。 または、最新の修正プログラムを適用することもできます。

     > [!IMPORTANT]
    > この手順により、ダウンタイムが発生するため、しばらくの間環境を使用できなくなる可能性があることを確認してください。 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]