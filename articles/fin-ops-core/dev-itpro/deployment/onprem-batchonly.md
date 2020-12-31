---
title: オンプレミス配置でのバッチのみおよび対話型のみの AOS ノードのコンフィギュレーション
description: このトピックでは、環境をコンフィギュレーションして、バッチのみおよび対話型のみの AOS ノードを配置できるようにする方法について説明します。
author: faix
manager: AnnBe
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4c6f7b558be86ae975f26d960c01d065ff7a920e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685457"
---
# <a name="configure-batch-only-and-interactive-only-aos-nodes-in-on-premises-deployments"></a><span data-ttu-id="1eb02-103">オンプレミス配置でのバッチのみおよび対話型のみの AOS ノードのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1eb02-103">Configure Batch-only and Interactive-only AOS nodes in on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="1eb02-104">この機能は、アプリケーション更新 10.0.12 (プラットフォーム更新 36) 以降でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1eb02-104">This feature is supported starting in application update 10.0.12, Platform update 36.</span></span>

<span data-ttu-id="1eb02-105">このトピックでは、環境をコンフィギュレーションして、バッチのみおよび対話型のみの Application Object Server (AOS) ノードを配置できるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-105">This topic explains how to configure your environment so that you can deploy batch-only and interactive-only Application Object Server (AOS) nodes.</span></span>

<span data-ttu-id="1eb02-106">この機能を使用できるようにするために、Microsoft は 2 つの新しい Microsoft Azure Service Fabric ノード タイプを導入しました。</span><span class="sxs-lookup"><span data-stu-id="1eb02-106">To make this feature available, Microsoft has introduced two new Microsoft Azure Service Fabric node types.</span></span> <span data-ttu-id="1eb02-107">バッチ専用 AOS ノードの場合、新しいノード タイプは **BatchOnlyAOSNodeType** です。</span><span class="sxs-lookup"><span data-stu-id="1eb02-107">For batch-only AOS nodes, the new node type is **BatchOnlyAOSNodeType**.</span></span> <span data-ttu-id="1eb02-108">対話型のみの AOS ノードの場合、新しいノード タイプは **InteractiveOnlyAOSNodeType** です。</span><span class="sxs-lookup"><span data-stu-id="1eb02-108">For interactive-only AOS nodes, the new node type is **InteractiveOnlyAOSNodeType**.</span></span>

> [!NOTE]
> <span data-ttu-id="1eb02-109">従来の配置オプションでは、AOS ノードが対話型でバッチ ジョブを実行している場合でもサポートされますが、これらの変更による影響はありません。</span><span class="sxs-lookup"><span data-stu-id="1eb02-109">The traditional deployment option, where an AOS node is interactive and is running batch jobs, is still supported and isn't affected by these changes.</span></span>

## <a name="sizing"></a><span data-ttu-id="1eb02-110">サイズ変更</span><span class="sxs-lookup"><span data-stu-id="1eb02-110">Sizing</span></span>

<span data-ttu-id="1eb02-111">サンドボックス環境では、各タイプのノードを 2 つ以上使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1eb02-111">For sandbox environments, we recommend that you have at least two nodes of each type.</span></span>

<span data-ttu-id="1eb02-112">運用環境では、それぞれのタイプのノードを 3 つ以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1eb02-112">For production environments, there should be at least three nodes of each type.</span></span>

## <a name="new-deployments"></a><span data-ttu-id="1eb02-113">新しい配置</span><span class="sxs-lookup"><span data-stu-id="1eb02-113">New deployments</span></span>

1. <span data-ttu-id="1eb02-114">[オンプレミス環境の設定と配置](./setup-deploy-on-premises-pu12.md#describeconfig)で説明されているコンフィギュレーションを記述する場合は、**configtemplate.xml** ファイルを編集して新しいノード タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-114">When you're describing your configuration as explained in [Set up and deploy on-premises environments](./setup-deploy-on-premises-pu12.md#describeconfig), edit the **configtemplate.xml** file to add the new node types.</span></span> <span data-ttu-id="1eb02-115">完了すると、新しい **NodeType** セクションは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="1eb02-115">When you've finished, the new **NodeType** sections should resemble the following example.</span></span>

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

2. <span data-ttu-id="1eb02-116">[オンプレミス環境の設定と配置](./setup-deploy-on-premises-pu12.md#describeconfig)の残りの指示に通常どおりに従います。</span><span class="sxs-lookup"><span data-stu-id="1eb02-116">Follow the remaining instructions in [Set up and deploy on-premises environments](./setup-deploy-on-premises-pu12.md#describeconfig) in the usual way.</span></span>

## <a name="existing-deployments"></a><span data-ttu-id="1eb02-117">既存の配置</span><span class="sxs-lookup"><span data-stu-id="1eb02-117">Existing deployments</span></span>

1. <span data-ttu-id="1eb02-118">コンフィギュレーション ファイルを保存する時点まで、[AOS ノードの削除](onprem-remove-reinstall-AOS-node.md#option-1-use-a-configuration-file-preferred-option)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1eb02-118">Follow the instructions in [Remove an AOS node](onprem-remove-reinstall-AOS-node.md#option-1-use-a-configuration-file-preferred-option) up through the point where you save the configuration file.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1eb02-119">オプション 1「構成ファイルを使用する (推奨オプション)」を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1eb02-119">You must use option 1, "Use a configuration file (preferred option)."</span></span> <span data-ttu-id="1eb02-120">オプション 2 は使用 **しない** でください。</span><span class="sxs-lookup"><span data-stu-id="1eb02-120">Do **not** use option 2.</span></span>

2. <span data-ttu-id="1eb02-121">**ClusterConfig.json** ファイルの編集を続け、新しいノード タイプを **NodeTypes** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-121">Continue to edit the **ClusterConfig.json** file to add the new node types to the **NodeTypes** section.</span></span> <span data-ttu-id="1eb02-122">完了すると、**NodeTypes** セクションは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="1eb02-122">When you've finished, the **NodeTypes** section should resemble the following example.</span></span>

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

3. <span data-ttu-id="1eb02-123">クラスターからのノードの削除が完了するまで、停止したポイントから [AOS ノードの削除](onprem-remove-reinstall-AOS-node.md#option-1-use-a-configuration-file-preferred-option)の手順に引き続き従ってください。</span><span class="sxs-lookup"><span data-stu-id="1eb02-123">Continue to follow the instructions in [Remove an AOS node](onprem-remove-reinstall-AOS-node.md#option-1-use-a-configuration-file-preferred-option) from the point where you stopped until you've finished removing the nodes from your cluster.</span></span>
4. <span data-ttu-id="1eb02-124">Service Fabric Cluster から削除したコンピューターで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-124">On the machines that you've removed from the Service Fabric cluster, follow these steps:</span></span>

    1. <span data-ttu-id="1eb02-125">Service Fabric データ ルート (**C:\\ProgramData\\SF**) と Service Fabric ログ ルート (**C:\\ProgramData\\SF\\Log**) の内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-125">Delete the contents of your Service Fabric data root (**C:\\ProgramData\\SF**) and your Service Fabric log root (**C:\\ProgramData\\SF\\Log**).</span></span>
    2. <span data-ttu-id="1eb02-126">Windows Server 用 Service Fabric のスタンドアロン パッケージをバーチャル マシン (VM) またはコンピューターにコピーまたはダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1eb02-126">Copy or download the standalone package for Service Fabric for Windows Server to the virtual machine (VM) or machine.</span></span>
    3. <span data-ttu-id="1eb02-127">パッケージを解凍します (**C:\\Temp\\ServiceFabricStandalone**)。</span><span class="sxs-lookup"><span data-stu-id="1eb02-127">Unzip the package (**C:\\Temp\\ServiceFabricStandalone**).</span></span>
    4. <span data-ttu-id="1eb02-128">Windows PowerShell を管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="1eb02-128">Open Windows PowerShell as an admin.</span></span>
    5. <span data-ttu-id="1eb02-129">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-129">Run the following commands.</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="1eb02-130">使用しているコンピューター コンフィギュレーションのパラメーターを必要に応じて置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1eb02-130">Replace parameters as appropriate for your machine configuration.</span></span>

        ```powershell
        cd C:\Temp\ServiceFabricStandalone
        .\AddNode.ps1 -NodeName AOS_12 -NodeType BatchOnlyAOSNodeType -NodeIpAddressOrFQDN 192.168.5.12 -ExistingClientConnectionEndpoint 192.168.5.21:19000 -UpgradeDomain ud0 -FaultDomain fd:/fd0 -X509Credential -ServerCertThumbprint 1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A -AcceptEULA -StoreLocation LocalMachine -StoreName MY -FindValueThumbprint 1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A1A
        ```

        > [!NOTE]
        > <span data-ttu-id="1eb02-131">最初にノードが Service Fabric Explorer に再表示されたときは、古いノード タイプが表示されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1eb02-131">When the node first reappears in Service Fabric Explorer, it might show the old node type.</span></span> <span data-ttu-id="1eb02-132">ただし、数分後に更新されたノード タイプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1eb02-132">However, it should show the updated node type after a few minutes.</span></span>

5. <span data-ttu-id="1eb02-133">**ClusterConfig.json** ファイルについて、Service Fabric Cluster を再度照会します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-133">Query the Service Fabric cluster again for the **ClusterConfig.json** file.</span></span>

    ```powershell
    Get-ServiceFabricClusterConfiguration -UseApiVersion -ApiVersion 10-2017 > C:\Temp\ClusterConfig.json
    ```

6. <span data-ttu-id="1eb02-134">**fabricSettings** セクションで、**NodesToBeRemoved** パラメーターを削除します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-134">In the **fabricSettings** section, remove the **NodesToBeRemoved** parameter.</span></span> <span data-ttu-id="1eb02-135">完了すると、**fabricSettings** セクションは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="1eb02-135">When you've finished, the **fabricSettings** section should resemble the following example.</span></span>

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

7. <span data-ttu-id="1eb02-136">**セキュリティ** セクションから次の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-136">Remove the following lines from the **Security** section.</span></span>

    ```json
    "WindowsIdentities": {
        "\$id": "3"
    },
    ```

    > [!NOTE]
    > <span data-ttu-id="1eb02-137">これらの行を削除しないと、後続の処理でで次のエラーメッセージが表示されます：</span><span class="sxs-lookup"><span data-stu-id="1eb02-137">If you don't remove these lines, you will receive the following error message later:</span></span>
    >
    > <span data-ttu-id="1eb02-138">*ValidationException: 認証タイプをセキュリティで保護されていないものから Windows に変更することはできません。*</span><span class="sxs-lookup"><span data-stu-id="1eb02-138">*ValidationException: Authentication type can't be changed from unsecured to Windows.*</span></span>

8. <span data-ttu-id="1eb02-139">構成ファイルのバージョン番号をインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="1eb02-139">Increment the version number of the configuration file.</span></span> <span data-ttu-id="1eb02-140">この変更は最小限の増分で行ってください。</span><span class="sxs-lookup"><span data-stu-id="1eb02-140">Make this change at the lowest increment.</span></span> <span data-ttu-id="1eb02-141">次の例では、バージョン番号を **1.0.1** から **1.0.2** に変更しました。</span><span class="sxs-lookup"><span data-stu-id="1eb02-141">In the following example, the version number went from **1.0.1** to **1.0.2**.</span></span>

    ```json
    "ClusterConfigurationVersion": "1.0.2"
    ```

9. <span data-ttu-id="1eb02-142">構成ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-142">Save the configuration file.</span></span>
10. <span data-ttu-id="1eb02-143">管理者として Windows PowerShell を開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-143">Open Windows PowerShell as an admin, and run the following commands.</span></span>

    ```powershell
    Connect-ServiceFabricCluster
    Start-ServiceFabricClusterConfigurationUpgrade -ClusterConfigPath C:\Temp\ClusterConfig.json
    Update-ServiceFabricClusterUpgrade -UpgradeReplicaSetCheckTimeoutSec 30
    ```

11. <span data-ttu-id="1eb02-144">アップグレードを監視するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-144">To monitor the upgrade, you can run the following command.</span></span>

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

12. <span data-ttu-id="1eb02-145">LCS からのアップグレードが完了したら、環境の更新をトリガーするために設定を変更しないで [設定の更新] ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="1eb02-145">Once the upgrade is finished from LCS use the Update Settings button without changing any settings to trigger an environment refresh.</span></span> <span data-ttu-id="1eb02-146">または、最新の修正プログラムを適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="1eb02-146">Alternatively you could also apply the latest hotfix.</span></span>

     > [!IMPORTANT]
    > <span data-ttu-id="1eb02-147">この手順により、ダウンタイムが発生するため、しばらくの間環境を使用できなくなる可能性があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1eb02-147">This step causes downtime so be sure that your environment can be unavailable for some time.</span></span> 

