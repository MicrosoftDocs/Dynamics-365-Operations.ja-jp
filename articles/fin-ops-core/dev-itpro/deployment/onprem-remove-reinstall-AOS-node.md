---
title: AOS ノードの削除と再インストール、または追加
description: このトピックでは、オンプレミス環境の アプリケーション オブジェクト サーバー (AOS) ノードを削除して、障害が発生したノードの削減または交換をする方法について説明します。 新たなノードを作成する方法についても説明します。
author: ttreen
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Platform update 34
ms.openlocfilehash: 021dec02ef382f384ddcc8f76f115b719f712988
ms.sourcegitcommit: 2d3c757f453fcb07df629f86de4ea0c94f1370aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/15/2020
ms.locfileid: "3264300"
---
# <a name="remove-and-reinstall-or-add-an-aos-node"></a><span data-ttu-id="0814b-104">AOS ノードの削除と再インストール、または追加</span><span class="sxs-lookup"><span data-stu-id="0814b-104">Remove and reinstall, or add an AOS node</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0814b-105">このトピックでは、オンプレミス環境の アプリケーション オブジェクト サーバー (AOS) ノードを削除して、障害が発生したノードの削減または交換をする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0814b-105">This topic explains how to remove an Application Object Server (AOS) node in your on-premises environment to reduce or replace a failed node.</span></span> <span data-ttu-id="0814b-106">また、スケール アウト パフォーマンスの新しい AOS ノードを追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="0814b-106">It also explains how to add a new AOS node for scale-out performance.</span></span>

## <a name="remove-a-node"></a><span data-ttu-id="0814b-107">ノードの削除</span><span class="sxs-lookup"><span data-stu-id="0814b-107">Remove a node</span></span>

### <a name="option-1-use-a-configuration-file-preferred-option"></a><span data-ttu-id="0814b-108">オプション 1：構成ファイルを使用する (推奨オプション)</span><span class="sxs-lookup"><span data-stu-id="0814b-108">Option 1: Use a configuration file (preferred option)</span></span>

<span data-ttu-id="0814b-109">**参照ドキュメント：**[Windows Server で実行されているスタンドアローンの Service Fabric Cluster へのノードの追加または削除](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-windows-server-add-remove-nodes)</span><span class="sxs-lookup"><span data-stu-id="0814b-109">**Reference document:** [Add or remove nodes to a standalone Service Fabric cluster running on Windows Server](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-windows-server-add-remove-nodes)</span></span>

1. <span data-ttu-id="0814b-110">Service Fabric エクスプローラー で、**クラスター** を選択し、Microsoft Service Fabric Cluster のバージョンをメモします。</span><span class="sxs-lookup"><span data-stu-id="0814b-110">In Service Fabric Explorer, select **Cluster**, and make a note of the Microsoft Service Fabric cluster version.</span></span> <span data-ttu-id="0814b-111">この例では、クラスター バージョンが **6.5.676.9590** となっています。</span><span class="sxs-lookup"><span data-stu-id="0814b-111">For this example, the cluster version is **6.5.676.9590**.</span></span>

    ![クラスター バージョン](media/fe0c857aefd3a1174df38f8e0c644667.png)

2. <span data-ttu-id="0814b-113">いずれかのオーケストレータノード ノードで、ファイル エクスプローラーを開きます。</span><span class="sxs-lookup"><span data-stu-id="0814b-113">On one of the orchestrator nodes, open File Explorer.</span></span> <span data-ttu-id="0814b-114">**表示** タブの、**表示/非表示** グループで、**ファイル名の拡張子** と **非表示項目** の各チェック ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0814b-114">On the **View** tab, in the **Show/hide** group, make sure that the **File name extensions** and **Hidden items** check boxes are selected.</span></span>

    ![オプションの表示](media/bb83d249cdce333bdbb2e276ebce559c.png)

3. <span data-ttu-id="0814b-116">ドライブ C を展開し、次のフォルダにドリル ダウンします。</span><span class="sxs-lookup"><span data-stu-id="0814b-116">Expand drive C, and then drill down into the following folder.</span></span> <span data-ttu-id="0814b-117">（パスの太字部分は、ノード名と設定によって異なることに注意してください）</span><span class="sxs-lookup"><span data-stu-id="0814b-117">(Note that the bold parts of the path will vary, depending on the node name and setup.)</span></span>

    <span data-ttu-id="0814b-118">C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**</span><span class="sxs-lookup"><span data-stu-id="0814b-118">C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**</span></span>

    <span data-ttu-id="0814b-119">このフォルダーには、Microsoft Service Fabric のさまざまなバージョンのフォルダがリスト表示されます。</span><span class="sxs-lookup"><span data-stu-id="0814b-119">In the folder, you should see a list of folders for various versions of Microsoft Service Fabric.</span></span> <span data-ttu-id="0814b-120">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="0814b-120">Here is an example.</span></span>

    ![131811633624852852 フォルダの内容](media/f843b5ceda67f767f54333851f5deeec.png)

5. <span data-ttu-id="0814b-122">前述の手順でメモした Microsoft Service Fabric Cluster のバージョンと同じ名前のフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="0814b-122">Open the folder with the name the same as the version of Microsoft Service Fabric cluster you that you made a note of earlier.</span></span> <span data-ttu-id="0814b-123">この例では、フォルダの名称が **6.5.676.9590** となっています。</span><span class="sxs-lookup"><span data-stu-id="0814b-123">For this example, the folder is named **6.5.676.9590**.</span></span>
6. <span data-ttu-id="0814b-124">フォルダ内に .cab ファイルが表示されています。</span><span class="sxs-lookup"><span data-stu-id="0814b-124">In the folder, you should see a .cab file.</span></span>

    ![6.5.676.9590 フォルダの内容](media/fd04e00bc3d940f5637900e46db8f134.png)

7. <span data-ttu-id="0814b-126">.Cab ファイルを C:\\Temp にコピーし、コピーしたファイルを **MicrosoftAzureServiceFabric.cab** に変更します。</span><span class="sxs-lookup"><span data-stu-id="0814b-126">Copy the .cab file to C:\\Temp, and rename the copied file **MicrosoftAzureServiceFabric.cab**.</span></span> <span data-ttu-id="0814b-127">（Temp フォルダーがない場合は作成してください）</span><span class="sxs-lookup"><span data-stu-id="0814b-127">(If you don't have a Temp folder, create it.)</span></span>

    ![Temp フォルダーにコピーされて名前変更されたファイル](media/e146a300f030d0695be858d8c7261486.png)

8. <span data-ttu-id="0814b-129">Windows PowerShell のコマンドプロンプトを管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="0814b-129">Open a Windows PowerShell Command Prompt window as an admin.</span></span>
9. <span data-ttu-id="0814b-130">次のコマンドを実行して、Service Fabric Cluster に接続します。</span><span class="sxs-lookup"><span data-stu-id="0814b-130">Run the following command to connect to the Service Fabric cluster.</span></span>

    ```powershell
    #Connect to Service Fabric Cluster. Replace 123 with server/star thumbprint and use appropriate IP address
    Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123
    ```

    ![接続コマンドと結果](media/0af2777b388b786d2ba6fe0b1f0f77dc.png)

10. <span data-ttu-id="0814b-132">次のコマンドを実行して、構成ファイルを C:\\Temp\\ClusterConfig.json に保存します。</span><span class="sxs-lookup"><span data-stu-id="0814b-132">Run the following command to save the configuration file to C:\\Temp\\ClusterConfig.json.</span></span> <span data-ttu-id="0814b-133">（C:\\Temp のパスが存在することを確認してください）</span><span class="sxs-lookup"><span data-stu-id="0814b-133">(Make sure that the C:\\Temp path exists.)</span></span>

    ```powershell
    Get-ServiceFabricClusterConfiguration -UseApiVersion -ApiVersion 10-2017 >C:\Temp\ClusterConfig.json
    ```

11. <span data-ttu-id="0814b-134">上記の手順で保存した構成ファイルで、**fabricSettings** セクションの **設定** セクションで、**NodesToBeRemoved** パラメーターのセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="0814b-134">In the configuration file that you saved in the previous step, in the **fabricSettings** section, in the **Setup** section, add a section for the **NodesToBeRemoved** parameter.</span></span> <span data-ttu-id="0814b-135">パラメータ値は、削除するノードの名前をカンマで区切ったリストにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0814b-135">The parameter value should be a comma-separated list of names of the nodes that must be removed.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0814b-136">新たなセクションの前の行の末尾には、必ずコンマを追加してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-136">Be sure to add a comma to the end of the line that precedes the new section.</span></span>

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
                },
                {
                    "name": "NodesToBeRemoved",
                    "value": "AOS1"
                }
            ]
        }
    ]
    ```

12. <span data-ttu-id="0814b-137">**ノード** セクションからノードを削除します。</span><span class="sxs-lookup"><span data-stu-id="0814b-137">Remove the node from the **Nodes** section.</span></span> <span data-ttu-id="0814b-138">次の例では、**AOS1** ノードが削除されています。</span><span class="sxs-lookup"><span data-stu-id="0814b-138">In the following example, the **AOS1** node was removed.</span></span>

    ```json
    "Nodes": [
        {
            "NodeName": "AOS2",
            "NodeTypeRef": "AOSNodeType",
            "IPAddress": "10.0.0.10",
            "FaultDomain": "fd:/fd1",
            "UpgradeDomain": "ud1"
        },
        {
        "NodeName": "AOS3",
        "NodeTypeRef": "AOSNo…
    ```

13. <span data-ttu-id="0814b-139">**セキュリティ** セクションから次の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="0814b-139">Remove the following lines from the **Security** section.</span></span>

    ```json
    "WindowsIdentities": {
        "\$id": "3"
    },
    ```

    > [!NOTE]
    > <span data-ttu-id="0814b-140">これらの行を削除しないと、後続の処理でで次のエラーメッセージが表示されます：</span><span class="sxs-lookup"><span data-stu-id="0814b-140">If you don't remove these lines, you will receive the following error message later:</span></span>
    >
    > <span data-ttu-id="0814b-141">ValidationException: 認証タイプをセキュリティで保護されていないものから Windows に変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="0814b-141">ValidationException: Authentication type can't be changed from unsecured to Windows.</span></span>

14. <span data-ttu-id="0814b-142">構成ファイルのバージョン番号をインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="0814b-142">Increment the version number of the configuration file.</span></span> <span data-ttu-id="0814b-143">この変更は最小限の増分で行ってください。</span><span class="sxs-lookup"><span data-stu-id="0814b-143">Make this change at the lowest increment.</span></span> <span data-ttu-id="0814b-144">次の例では、バージョン番号を **1.0.0** から **1.0.1** に変更しました。</span><span class="sxs-lookup"><span data-stu-id="0814b-144">In the following example, the version number went from **1.0.0** to **1.0.1**.</span></span>

    ```json
    "ClusterConfigurationVersion": "1.0.1"
    ```

15. <span data-ttu-id="0814b-145">構成ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="0814b-145">Save the configuration file.</span></span>
16. <span data-ttu-id="0814b-146">次のコマンドを実行してノードを削除します。</span><span class="sxs-lookup"><span data-stu-id="0814b-146">Run the following command to remove the node.</span></span>

    ```powershell
    Start-ServiceFabricClusterConfigurationUpgrade -ClusterConfigPath C:\Temp\ClusterConfig.json
    ```

17. <span data-ttu-id="0814b-147">次のコマンドを実行し進捗の監視をします。</span><span class="sxs-lookup"><span data-stu-id="0814b-147">Run the following command to monitor the progress.</span></span>

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

    <span data-ttu-id="0814b-148">"UpgradePhase: PreUpgradeSafetyCheck," でアップグレードが応答しなくなった場合は、**NodeName** の値をメモして、Service Fabric エクスプローラー からそのノードを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-148">If the upgrade stops responding at "UpgradePhase: PreUpgradeSafetyCheck," make a note of the **NodeName** value, and restart that node from Service Fabric Explorer.</span></span> <span data-ttu-id="0814b-149">以下の図では、アップグレードが応答を停止しています。</span><span class="sxs-lookup"><span data-stu-id="0814b-149">In the following illustration, the upgrade has stopped responding.</span></span> <span data-ttu-id="0814b-150">ノード BI1 では同じ状態のままで、50分間実行されていました。</span><span class="sxs-lookup"><span data-stu-id="0814b-150">It was running for 50 minutes at the same status on node BI1.</span></span>

    ![応答が停止したアップグレード](media/c9a57cd8a5828a63a010d829eaab597c.png)

    <span data-ttu-id="0814b-152">クラスタ構成のアップグレード中に、**Add-ServiceFabricNode** コマンドを使用して既にノードが追加されているというエラーメッセージが表示された場合は、バージョン番号以外の構成ファイルを変更せずに構成のアップグレードを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0814b-152">During upgrade of the cluster configuration, if you receive an error message that states that you previously added a node through the **Add-ServiceFabricNode** command, you will need to run a configuration upgrade without making any changes to the configuration file except for the version number.</span></span> <span data-ttu-id="0814b-153">この目的では、**Get-ServiceFabricClusterConfiguration** と **Start-ServiceFabricClusterConfigurationUpgrade** コマンドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0814b-153">You can use the **Get-ServiceFabricClusterConfiguration** and **Start-ServiceFabricClusterConfigurationUpgrade** commands for this purpose.</span></span>

    ![コマンドと結果の取得](media/329b9c2bd807d7bca96e106037504e0e.png)

    <span data-ttu-id="0814b-155">また、 Service Fabric エクスプローラー で進行状況を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="0814b-155">You can also view the progress in Service Fabric Explorer.</span></span>

    ![Service Fabric エクスプローラー の進行状況に関する情報](media/99c6321f9da950d91a1709cae2473d97.png)

### <a name="option-2-use-service-fabric-explorer"></a><span data-ttu-id="0814b-157">オプション 2：Service Fabric エクスプローラー の使用</span><span class="sxs-lookup"><span data-stu-id="0814b-157">Option 2: Use Service Fabric Explorer</span></span>

1. <span data-ttu-id="0814b-158">Service Fabric エクスプローラーにログインします。</span><span class="sxs-lookup"><span data-stu-id="0814b-158">Sign in to Service Fabric Explorer.</span></span>
2. <span data-ttu-id="0814b-159">**設定** ボタン (歯車記号) を選択し、**詳細** モードがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0814b-159">Select the **Settings** button (gear symbol), and make sure that **Advanced** mode is turned on.</span></span>

    ![詳細モードがオンになっている場合](media/bc25caaed54da595a3c75429faaf73cb.png)

3. <span data-ttu-id="0814b-161">**ノード** を展開し、省略記号（**...**）ボタンをクリックし、**非アクティブ化（データの削除）** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0814b-161">Expand **Nodes**, select the ellipsis (**...**) button next to the node that you want to remove, and then select **Deactivate (remove data)**.</span></span> <span data-ttu-id="0814b-162">このオプションは、ノードがすでにダウンしている場合 (ノード サーバーが起動できない場合など) には使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-162">Note that this option might not be available if the node is already down (for example, if the node server can't be started).</span></span>

    ![データの無効化（データの削除）コマンド](media/6865310acd6150cc81ee4a56aaeeed3f.png)

4. <span data-ttu-id="0814b-164">無効化の確認が求められた際は、ノードの名前を入力し、**非アクティブ化（データの削除）** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0814b-164">When you're prompted to confirm deactivation, enter the name of the node, and then select **Deactivate (remove data)**.</span></span>

    ![ノードの無効化を確認する](media/49486a44d04b7a91431f18beebda43e8.png)

    <span data-ttu-id="0814b-166">ノードが非アクティブ化されると、状態が **無効** と表示されます。</span><span class="sxs-lookup"><span data-stu-id="0814b-166">After the node has been deactivated, its status is shown as **Disabled**.</span></span>

    ![無効な状態のノード](media/4dba61b4c22966cb4098cf832a4e5e90.png)

5. <span data-ttu-id="0814b-168">サーバーがまだ有効でドメインに接続されている場合、無効化されたノードを新しいサーバーに置き換える場合は、以下の手順を実行することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="0814b-168">If the server is still active and connected to the domain, you might have to follow these steps if you will be replacing the deactivated node with a new server:</span></span>

    1. <span data-ttu-id="0814b-169">サーバーにサイン インします。</span><span class="sxs-lookup"><span data-stu-id="0814b-169">Sign in to the server.</span></span>
    2. <span data-ttu-id="0814b-170">ドメインからサーバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="0814b-170">Remove the server from the domain.</span></span>
    3. <span data-ttu-id="0814b-171">サーバー名を変更します。</span><span class="sxs-lookup"><span data-stu-id="0814b-171">Rename the server.</span></span>
    4. <span data-ttu-id="0814b-172">IP アドレスを書き留めてから、IP アドレスを範囲内の空いているアドレスに変更します。</span><span class="sxs-lookup"><span data-stu-id="0814b-172">Make a note of the IP address, and then change the IP address to a free address that you have in your range.</span></span>
    5. <span data-ttu-id="0814b-173">サーバーをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="0814b-173">Shut down the server.</span></span>

6. <span data-ttu-id="0814b-174">サーバーのシャットダウンの完了後、または既にダウンしていた場合は、Service Fabric エクスプローラーの状態が反映されます。</span><span class="sxs-lookup"><span data-stu-id="0814b-174">After the server has been shut down, or if it was already down, Service Fabric Explorer reflects its status.</span></span> <span data-ttu-id="0814b-175">省略符号（**...**）ボタンを再度クリックし、**ノードの状態を削除する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0814b-175">Select the ellipsis (**...**) button again next to the node, and then select **Remove node state**.</span></span>

    ![ノードの状態を削除するコマンド](media/e0460a280693cdf13896731aa7f2377f.png)

7. <span data-ttu-id="0814b-177">ノードを削除することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0814b-177">Confirm removal of the node.</span></span>

    ![ノードの削除を確認します](media/a711e04b14b8adddc5d3941f010b32e0.png)

    <span data-ttu-id="0814b-179">ノードが削除されると、状態が **無効** と表示されます。</span><span class="sxs-lookup"><span data-stu-id="0814b-179">After the node has been removed, its status is shown as **Invalid**.</span></span>

    ![無効な状態のノード](media/c3f8dc79d51e535074e89dfca04006b8.png)

8. <span data-ttu-id="0814b-181">ノードの名前とタイプをメモします。</span><span class="sxs-lookup"><span data-stu-id="0814b-181">Make a note of the node name and type.</span></span> <span data-ttu-id="0814b-182">この例では、ノード名は **AOS1** で、タイプは **AOSNodeType** です。</span><span class="sxs-lookup"><span data-stu-id="0814b-182">For this example, the node name is **AOS1**, and the type is **AOSNodeType**.</span></span> <span data-ttu-id="0814b-183">ノード名がネットワーク名と一致しない可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-183">Remember that the node name might not match the network name.</span></span> <span data-ttu-id="0814b-184">また、**ドメインのアップグレード** と **障害ドメイン** の設定、およびIPアドレスについてもメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="0814b-184">Also make a note of the **Upgrade Domain** and **Fault Domain** settings, and the IP address.</span></span> <span data-ttu-id="0814b-185">上記の図にはこれらの値がすべて表示されています。</span><span class="sxs-lookup"><span data-stu-id="0814b-185">The previous illustration shows all these values.</span></span>

## <a name="add-a-node"></a><span data-ttu-id="0814b-186">ノードの追加</span><span class="sxs-lookup"><span data-stu-id="0814b-186">Add a node</span></span>

<span data-ttu-id="0814b-187">次の手順では、新しい AOS サーバーを起動します。</span><span class="sxs-lookup"><span data-stu-id="0814b-187">The next step is to start a new AOS server.</span></span>

1. <span data-ttu-id="0814b-188">削除された既存のサーバーを置き換える場合は、次の手順に従います：</span><span class="sxs-lookup"><span data-stu-id="0814b-188">Follow these steps if you're replacing an existing server that was removed:</span></span>

    1. <span data-ttu-id="0814b-189">以前の AOS サーバーのネットワーク名をサーバーに設定します。</span><span class="sxs-lookup"><span data-stu-id="0814b-189">Give the server the network name of the previous AOS server.</span></span>
    2. <span data-ttu-id="0814b-190">元の IP アドレスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0814b-190">Assign the original IP address.</span></span> <span data-ttu-id="0814b-191">この例では、IP アドレスを **10.0.0.9** としています。</span><span class="sxs-lookup"><span data-stu-id="0814b-191">For this example, that IP address is **10.0.0.9**.</span></span>
    3. <span data-ttu-id="0814b-192">サーバーをドメインに追加します。</span><span class="sxs-lookup"><span data-stu-id="0814b-192">Join the server to the domain.</span></span>

2. <span data-ttu-id="0814b-193">既存のクラスターに新しいサーバーを追加する場合は、ConfigTemplate .xml ファイルを更新することで追加情報を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0814b-193">If you're adding a new server to an existing cluster, update the ConfigTemplate.xml file so that it contains the additional information.</span></span> <span data-ttu-id="0814b-194">この情報は、前提条件を押し出して、Windows PowerShell スクリプトを使用して設定を適用する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0814b-194">This information will be used when you push out the prerequisites and apply settings through Windows PowerShell scripts.</span></span>
3. <span data-ttu-id="0814b-195">AOS サーバーのローカル管理者グループに **AXServiceUser** と **svc-AXSF\$** グループのマネージド サービス アカウント (gMSA) が追加されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-195">Make sure that you've added the **AXServiceUser** and **svc-AXSF\$** group Managed Service Accounts (gMSAs) to the local admin group on the AOS server.</span></span>

    <span data-ttu-id="0814b-196">サーバーをドメインに接続した後は、[オンプレミス環境 (プラットフォーム更新プログラム 12 以降) の設定と展開](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu12#follow-these-steps-for-each-vm-or-use-remoting-from-a-single-machine) に記載されているオンプレミス環境の前提条件に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0814b-196">After the server is connected to the domain, you must follow the prerequisite steps for on-premises environments in [Set up and deploy on-premises environments (Platform update 12 and later)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu12#follow-these-steps-for-each-vm-or-use-remoting-from-a-single-machine).</span></span> <span data-ttu-id="0814b-197">次の手順は、これら前提条件の手順をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="0814b-197">The following steps summarize those prerequisite steps.</span></span>

4. <span data-ttu-id="0814b-198">それぞれの、インフラストラクチャ\\VM\<VM名\> フォルダの内容を、対応する仮想マシン (VM) にコピーします。</span><span class="sxs-lookup"><span data-stu-id="0814b-198">Copy the contents of each infrastructure\\VMs\<VMName\> folder into the corresponding virtual machine (VM).</span></span> <span data-ttu-id="0814b-199">（リモート スクリプトを使用している場合は、コンテンツが自動的に対象のVMにコピーされます。）続いて、次の Windows PowerShell スクリプトを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="0814b-199">(If you use remoting scripts, they will automatically copy the contents to the target VMs.) Then run the following Windows PowerShell scripts as an admin.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0814b-200">リモートで実行している既存のサーバーを修復する場合は、すべてのサーバーに対してファイルコピー処理が実行されるように、[インフラストラクチャ] フォルダから lbdscripts_remote_status.json ファイルを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0814b-200">If you're running remotely and repairing an existing server, you must delete the lbdscripts_remote_status.json file from the infrastructure folder to ensure the file copy process is run against all servers again.</span></span>

    ```powershell
    # Install pre-req software on the VMs.
    # If Remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml
    .\Configure-PreReqs.ps1 -MSIFilePath <share folder path of the MSIs>
    ```

5. <span data-ttu-id="0814b-201">再起動を求めるメッセージが表示されるたびにコンピューターを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-201">Restart the computer every time that you're prompted.</span></span> <span data-ttu-id="0814b-202">すべての前提条件がインストールされるまでは、再起動後に  **.\\Configure-PreReqs.ps1**   スクリプトを必ず再実行してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-202">Make sure that you rerun the **.\\Configure-PreReqs.ps1** script after every restart, until all the prerequisites are installed.</span></span> <span data-ttu-id="0814b-203">リモート処理の場合、すべてのコンピューターがオンラインに戻った際に **AllVMs** スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="0814b-203">In the case of remoting, rerun the **AllVMs** script when all the computers are back online.</span></span>
6. <span data-ttu-id="0814b-204">リモート処理スクリプトを使用する場合は、現在のユーザーが Microsoft Windows インストーラー パッケージ ファイル (.msiファイル) の共有フォルダにアクセスできることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-204">If you use the remoting script, make sure that the current user has access to the share folder of Microsoft Windows Installer package files (.msi files).</span></span>
7. <span data-ttu-id="0814b-205">リモート処理スクリプトを使用する場合は、ユーザーが **AOSNodeType**、**MRType**、**ReportServerType** タイプのコンピューターにアクセスしていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-205">If you use the remoting script, make sure that no user is accessing computers of the **AOSNodeType**, **MRType**, and **ReportServerType** types.</span></span> <span data-ttu-id="0814b-206">この条件に当てはまる場合は、ユーザーがログインしている理由によって、リモートスクリプトがコンピューターを再起動できなくなります。</span><span class="sxs-lookup"><span data-stu-id="0814b-206">Otherwise, the remoting script won't be able to restart the computer because users are signed in to it.</span></span>
8. <span data-ttu-id="0814b-207">VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="0814b-207">Run the following scripts, if they exist, to complete the VM setup.</span></span>

    ```powershell
    # If Remoting, only execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

9. <span data-ttu-id="0814b-208">**Add-GMSAonVM.ps1** の実行中にエラーが発生した場合は、次のコマンドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0814b-208">If errors occur while you run **Add-GMSAonVM.ps1**, you must run the following command.</span></span> <span data-ttu-id="0814b-209">（サービスア カウントが異なる場合は、このコマンドを編集してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-209">(Edit the command if your service account differs.</span></span> <span data-ttu-id="0814b-210">ドル記号 \[\$\] をサービスアカウント名から削除することを忘れないでください。）</span><span class="sxs-lookup"><span data-stu-id="0814b-210">Note that you remove the dollar sign \[\$\] from the service account name.)</span></span>

    ```powershell
    Get-ADServiceAccount -Identity svc-AXSF -properties PrincipalsAllowedToRetrieveManagedPassword
    ```

    ![コマンドと結果の取得](media/525f31b6281e87fd58075f2101f75118.png)

    <span data-ttu-id="0814b-212">**svc-AXFS\$** gMSA のパスワードを取得するにあたって、アクセス許可が与えられているサーバーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0814b-212">You see a list of the servers that have permission to retrieve the password for the **svc-AXFS\$** gMSA.</span></span> <span data-ttu-id="0814b-213">削除されたサーバーのグローバル一意識別子 (GUID) 値が表示される場合は、無視します。</span><span class="sxs-lookup"><span data-stu-id="0814b-213">If you see a globally unique identifier (GUID) value for the server that was removed, ignore it.</span></span>

10. <span data-ttu-id="0814b-214">結果からプリンシパルの一覧をコピーし、それを使用して次のコマンドを編集または修正します。</span><span class="sxs-lookup"><span data-stu-id="0814b-214">Copy the list of principals from the result, and use them to edit or amend the following command.</span></span> <span data-ttu-id="0814b-215">（**Set** コマンドは付加されないため、すべての参照に再度追加する必要があります）</span><span class="sxs-lookup"><span data-stu-id="0814b-215">(Note that, because the **Set** command isn't additive, you must add all references back in.)</span></span>

    ```powershell
    Set-ADServiceAccount -Identity svc-AXSF -PrincipalsAllowedToRetrieveManagedPassword  "CN=AOS1,CN=Computers,DC=contoso,DC=com","CN=AOS2,CN=Computers,DC=contoso,DC=com","CN=AOS3,CN=Computers,DC=contoso,DC=com"
    ```

    ![コマンドの設定](media/ff652391b87c72cacd318b588758e4fc.png)

11. <span data-ttu-id="0814b-217">元 **Get** コマンドを実行して、新たな AOS ノードが再度追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="0814b-217">Run the original **Get** command to verify that the new AOS node was added back in.</span></span> <span data-ttu-id="0814b-218">（この後の例では、AOS1 が PrincipalsAllowedToRetrieveManagedPassword の一覧に追加されていることが確認できます）</span><span class="sxs-lookup"><span data-stu-id="0814b-218">(Note in the example screenshot below you can see that AOS1 was added to the list of PrincipalsAllowedToRetrieveManagedPassword.)</span></span>

    ![元の Get コマンドと結果](media/17b9c379b6328ed506d16270280146f4.png)

12. <span data-ttu-id="0814b-220">次のスクリプトを実行して VM のセットアップを検証します。</span><span class="sxs-lookup"><span data-stu-id="0814b-220">Run the following script to validate the VM setup.</span></span>

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    .\Test-D365FOConfiguration.ps1
    ```

13. <span data-ttu-id="0814b-221">続行する前に、検証スクリプトの一環として失敗する箇所を修正してください。</span><span class="sxs-lookup"><span data-stu-id="0814b-221">Before you continue, fix anything that fails as part of the validation script.</span></span>
14. <span data-ttu-id="0814b-222">Service Fabric エクスプローラー で、**クラスター** を選択し、Microsoft Service Fabric Cluster のバージョンをメモします。</span><span class="sxs-lookup"><span data-stu-id="0814b-222">In Service Fabric Explorer, select **Cluster**, and make a note of the Microsoft Service Fabric cluster version.</span></span> <span data-ttu-id="0814b-223">この例では、クラスター バージョンが **6.5.676.9590** となっています。</span><span class="sxs-lookup"><span data-stu-id="0814b-223">For this example, the cluster version is **6.5.676.9590**.</span></span>

    ![クラスター バージョン](media/fe0c857aefd3a1174df38f8e0c644667.png)

15. <span data-ttu-id="0814b-225">いずれかのオーケストレータノード ノードで、ファイル エクスプローラーを開きます。</span><span class="sxs-lookup"><span data-stu-id="0814b-225">On one of the orchestrator nodes, open File Explorer.</span></span> <span data-ttu-id="0814b-226">**表示** タブの、**表示/非表示** グループで、**ファイル名の拡張子** と **非表示項目** の各チェック ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0814b-226">On the **View** tab, in the **Show/hide** group, make sure that the **File name extensions** and **Hidden items** check boxes are selected.</span></span>

    ![オプションの表示](media/bb83d249cdce333bdbb2e276ebce559c.png)

16. <span data-ttu-id="0814b-228">ドライブ C を展開し、次のフォルダにドリル ダウンします。</span><span class="sxs-lookup"><span data-stu-id="0814b-228">Expand drive C, and then drill down into the following folder.</span></span> <span data-ttu-id="0814b-229">（パスの太字部分は、ノード名と設定によって異なることに注意してください）</span><span class="sxs-lookup"><span data-stu-id="0814b-229">(Note that the bold parts of the path will vary, depending on the node name and setup.)</span></span>

    <span data-ttu-id="0814b-230">C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**</span><span class="sxs-lookup"><span data-stu-id="0814b-230">C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**</span></span>

    <span data-ttu-id="0814b-231">このフォルダーには、Service Fabric のさまざまなバージョンのフォルダがリスト表示されます。</span><span class="sxs-lookup"><span data-stu-id="0814b-231">In the folder, you should see a list of folders for various versions of Service Fabric.</span></span> <span data-ttu-id="0814b-232">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="0814b-232">Here is an example.</span></span>

    ![131811633624852852 フォルダの内容](media/f843b5ceda67f767f54333851f5deeec.png)

17. <span data-ttu-id="0814b-234">前述の手順でメモした Microsoft Service Fabric Cluster のバージョンと同じ名前のフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="0814b-234">Open the folder that has the same name as the version of Microsoft Service Fabric cluster that you made a note of earlier.</span></span> <span data-ttu-id="0814b-235">この例では、フォルダの名称が **6.5.676.9590** となっています。</span><span class="sxs-lookup"><span data-stu-id="0814b-235">For this example, the folder is named **6.5.676.9590**.</span></span>
18. <span data-ttu-id="0814b-236">フォルダ内に .cab ファイルが表示されています。</span><span class="sxs-lookup"><span data-stu-id="0814b-236">In the folder, you should see a .cab file.</span></span>

    ![6.5.676.9590 フォルダの内容](media/fd04e00bc3d940f5637900e46db8f134.png)

19. <span data-ttu-id="0814b-238">.Cab ファイルを C:\\Temp にコピーし、コピーしたファイルを **MicrosoftAzureServiceFabric.cab** に変更します。</span><span class="sxs-lookup"><span data-stu-id="0814b-238">Copy the .cab file to C:\\Temp, and rename the copied file **MicrosoftAzureServiceFabric.cab**.</span></span> <span data-ttu-id="0814b-239">（Temp フォルダーがない場合は作成してください）</span><span class="sxs-lookup"><span data-stu-id="0814b-239">(If you don't have a Temp folder, create it.)</span></span>

    ![Temp フォルダーにコピーされて名前変更されたファイル](media/e146a300f030d0695be858d8c7261486.png)

20. <span data-ttu-id="0814b-241">Windows PowerShell のコマンドプロンプトを管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="0814b-241">Open a Windows PowerShell Command Prompt windows as an admin.</span></span>
21. <span data-ttu-id="0814b-242">次のコマンドを実行して、Service Fabric Cluster に接続します。</span><span class="sxs-lookup"><span data-stu-id="0814b-242">Run the following command to connect to your Service Fabric cluster.</span></span> <span data-ttu-id="0814b-243">（必要に応じてコマンドを編集します）</span><span class="sxs-lookup"><span data-stu-id="0814b-243">(Edit the command as you require.)</span></span>

    ```powershell
    #Connect to Service Fabric Cluster. Replace 123 with server/star thumbprint and use appropriate IP address
    Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123
    ```

    ![接続コマンドと結果](media/0af2777b388b786d2ba6fe0b1f0f77dc.png)

22. <span data-ttu-id="0814b-245">次のコマンドを実行して、ノードを追加し直します。</span><span class="sxs-lookup"><span data-stu-id="0814b-245">Run the following command to add the node back in.</span></span> <span data-ttu-id="0814b-246">実行前に、**NodeName**、**IPAddress**、**UpgradeDomain**、**FaultDomain** パラメータに対して必要な編集を行ってください。</span><span class="sxs-lookup"><span data-stu-id="0814b-246">Before you run it, make the required edits to the **NodeName**, **IPAddress**, **UpgradeDomain**, and **FaultDomain** parameters.</span></span> <span data-ttu-id="0814b-247">（既存のサーバーを置き換えている場合は、元の値をメモしておく必要があります）</span><span class="sxs-lookup"><span data-stu-id="0814b-247">(If you're replacing an existing server, you should have made a note of the values earlier.)</span></span>

    ```powershell
    Add-ServiceFabricNode -NodeName "AOS1" -NodeType "AOSNodeType" -IpAddressOrFQDN "10.0.0.9" -UpgradeDomain "ud0" -FaultDomain "fd:/fd0" -FabricRuntimePackagePath "C:\Temp\MicrosoftAzureServiceFabric.cab"
    ```

    ![コマンドと結果の追加](media/e8c153c1b8aa06af684a307f443c9b7b.png)

23. <span data-ttu-id="0814b-249">ノードを再追加した後は、Service Fabric エクスプローラーに戻り、アプリケーションの展開の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="0814b-249">After the node has been added back in, return to Service Fabric Explorer, and view the application deployment status.</span></span> <span data-ttu-id="0814b-250">すべての復元された AOS アプリケーション（**AXBootstrapperAppType**、**AXSFType**、**RTGatewayAppType**、**LBDTelemetryType-<envname\>** 、**MonitoringAgentAppType**）がプッシュ アウトされ、ノードにインストールされるには数分を要します。</span><span class="sxs-lookup"><span data-stu-id="0814b-250">Several minutes will be required before all the AOS applications are restored (**AXBootstrapperAppType**, **AXSFType**, **RTGatewayAppType**, and **LBDTelemetryType-<envname\>** or **MonitoringAgentAppType**) are pushed out again and installed on the node.</span></span>
