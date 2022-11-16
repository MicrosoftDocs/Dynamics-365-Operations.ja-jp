---
title: AOS ノードの削除と再インストール、または追加
description: この記事では、オンプレミス環境の Application Object Server (AOS) ノードを削除して、障害が発生したノードの削減または交換をする方法について説明します。
author: ttreen
ms.date: 07/28/2021
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Platform update 34
ms.openlocfilehash: 6cfb466471585c1b69497b83fb8dab8b64c979d5
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750750"
---
# <a name="remove-and-reinstall-or-add-an-aos-node"></a>AOS ノードの削除と再インストール、または追加

[!include[banner](../includes/banner.md)]

この記事では、オンプレミス環境の Application Object Server (AOS) ノードを削除して、障害が発生したノードの削減または交換をする方法について説明します。 また、スケール アウト パフォーマンスの新しい AOS ノードを追加する方法についても説明します。

## <a name="remove-a-node"></a>ノードの削除

### <a name="option-1-use-a-configuration-file-preferred-option"></a>オプション 1：構成ファイルを使用する (推奨オプション)

**参照ドキュメント：**[Windows Server で実行されているスタンドアローンの Service Fabric Cluster へのノードの追加または削除](/azure/service-fabric/service-fabric-cluster-windows-server-add-remove-nodes)

1. Service Fabric Explorer で、**クラスター** を選択し、Microsoft Service Fabric Cluster のバージョン (例: 8.2.1686.XXXX) をメモします
2. いずれかのオーケストレータノード ノードで、ファイル エクスプローラーを開きます。 **表示** タブの、**表示/非表示** グループで、**ファイル名の拡張子** と **非表示項目** の各チェック ボックスがオンになっていることを確認します。

    ![オプションを表示します。](media/bb83d249cdce333bdbb2e276ebce559c.png)

3. ドライブ C を展開し、次のフォルダにドリル ダウンします。 （パスの太字部分は、ノード名と設定によって異なることに注意してください）

    C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**

    このフォルダーには、Microsoft Service Fabric のさまざまなバージョンのフォルダがリスト表示されます。 

5. 前述の手順でメモした Microsoft Service Fabric Cluster のバージョンと同じ名前のフォルダーを開きます。 
6. フォルダ内に .cab ファイルが表示されています。
7. .Cab ファイルを C:\\Temp にコピーし、コピーしたファイルを **MicrosoftAzureServiceFabric.cab** に変更します。 （Temp フォルダーがない場合は作成してください）
8. Windows PowerShell のコマンドプロンプトを管理者として開きます。
9. 次のコマンドを実行して、Service Fabric Cluster に接続します。

    ```powershell
    #Connect to the Service Fabric Cluster
    Connect-ServiceFabricCluster 
    ```
10. 次のコマンドを実行して、構成ファイルを C:\\Temp\\ClusterConfig.json に保存します。 （C:\\Temp のパスが存在することを確認してください）

    ```powershell
    Get-ServiceFabricClusterConfiguration > C:\Temp\ClusterConfig.json
    ```

11. 上記の手順で保存した構成ファイルで、**fabricSettings** セクションの **設定** セクションで、**NodesToBeRemoved** パラメーターのセクションを追加します。 パラメータ値は、削除するノードの名前をカンマで区切ったリストにする必要があります。 

    > [!NOTE]
    > 新たなセクションの前の行の末尾には、必ずコンマを追加してください。

    ```json
    "fabricSettings": [
        {
            "name": "Setup",
            "parameters": [
                {
                    "name": "FabricDataRoot",
                    "value": "C:\\ProgramData\\SF"
                },
                {
                    "name": "FabricLogRoot",
                    "value": "C:\\ProgramData\\SF\\Log"
                },
                {
                    "name": "NodesToBeRemoved",
                    "value": "AOS1"
                }
            ]
        }
    ]
    ```

12. **ノード** セクションからノードを削除します。 次の例では、**AOS1** ノードが削除されています。

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

13. **セキュリティ** セクションから次の行を削除します。

    ```json
    "WindowsIdentities": {
        "\$id": "3"
    },
    ```

    > [!NOTE]
    > これらの行を削除しないと、後続の処理でで次のエラーメッセージが表示されます：
    >
    > ValidationException: 認証タイプをセキュリティで保護されていないものから Windows に変更することはできません。

14. 構成ファイルのバージョン番号をインクリメントします。 この変更は最小限の増分で行ってください。 次の例では、バージョン番号を **1.0.0** から **1.0.1** に変更しました。

    ```json
    "ClusterConfigurationVersion": "1.0.1"
    ```

15. 構成ファイルを保存します。
16. 次のコマンドを実行してノードを削除します。

    ```powershell
    Start-ServiceFabricClusterConfigurationUpgrade -ClusterConfigPath C:\Temp\ClusterConfig.json
    ```

17. 次のコマンドを実行し進捗の監視をします。

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

    "UpgradePhase: PreUpgradeSafetyCheck," でアップグレードが応答しなくなった場合は、**NodeName** の値をメモして、Service Fabric エクスプローラー からそのノードを再起動してください。 以下の図では、アップグレードが応答を停止しています。 ノード BI1 では同じ状態のままで、50分間実行されていました。

    クラスタ構成のアップグレード中に、**Add-ServiceFabricNode** コマンドを使用して既にノードが追加されているというエラーメッセージが表示された場合は、バージョン番号以外の構成ファイルを変更せずに構成のアップグレードを実行する必要があります。 この目的では、**Get-ServiceFabricClusterConfiguration** と **Start-ServiceFabricClusterConfigurationUpgrade** コマンドを使用することができます。

    また、 Service Fabric エクスプローラー で進行状況を確認することもできます。

### <a name="option-2-use-service-fabric-explorer"></a>オプション 2：Service Fabric エクスプローラー の使用

1. Service Fabric エクスプローラーにログインします。
2. **設定** ボタン (歯車記号) を選択し、**詳細** モードがオンになっていることを確認します。
3. **ノード** を展開し、省略記号（**...**）ボタンをクリックし、**非アクティブ化（データの削除）** を選択します。 このオプションは、ノードがすでにダウンしている場合 (ノード サーバーが起動できない場合など) には使用できないことに注意してください。
4. 無効化の確認が求められた際は、ノードの名前を入力し、**非アクティブ化（データの削除）** を選択します。

    ノードが非アクティブ化されると、状態が **無効** と表示されます。

5. サーバーがまだ有効でドメインに接続されている場合、無効化されたノードを新しいサーバーに置き換える場合は、以下の手順を実行することが必要な場合があります。

    1. サーバーにサイン インします。
    2. ドメインからサーバーを削除します。
    3. サーバー名を変更します。
    4. IP アドレスを書き留めてから、IP アドレスを範囲内の空いているアドレスに変更します。
    5. サーバーをシャットダウンします。

6. サーバーのシャットダウンの完了後、または既にダウンしていた場合は、Service Fabric エクスプローラーの状態が反映されます。 省略符号（**...**）ボタンを再度クリックし、**ノードの状態を削除する** を選択します。
7. ノードを削除することを確認します。

    ノードが削除されると、状態が **無効** と表示されます。

8. ノードの名前とタイプをメモします。 この例では、ノード名は **AOS1** で、タイプは **AOSNodeType** です。 ノード名がネットワーク名と一致しない可能性があることに注意してください。 また、**ドメインのアップグレード** と **障害ドメイン** の設定、およびIPアドレスについてもメモしておきます。 上記の図にはこれらの値がすべて表示されています。

## <a name="add-a-node"></a>ノードの追加

次の手順では、新しい AOS サーバーを起動します。

1. 削除された既存のサーバーを置き換える場合は、次の手順に従います：

    1. 以前の AOS サーバーのネットワーク名をサーバーに設定します。
    2. 元の IP アドレスを割り当てます。 この例では、IP アドレスを **10.0.0.9** としています。
    3. サーバーをドメインに追加します。

2. 既存のクラスターに新しいサーバーを追加する場合は、ConfigTemplate .xml ファイルを更新することで追加情報を含めることができます。 この情報は、前提条件を押し出して、Windows PowerShell スクリプトを使用して設定を適用する際に使用されます。
3. AOS サーバーのローカル管理者グループに **AXServiceUser** と **svc-AXSF\$** グループのマネージド サービス アカウント (gMSA) が追加されていることを確認してください。

    サーバーをドメインに接続した後は、[オンプレミス環境 (プラットフォーム更新プログラム 41 以降) の設定と展開](./setup-deploy-on-premises-pu41.md) に記載されているオンプレミス環境の前提条件に従う必要があります。 次の手順は、これら前提条件の手順をまとめたものです。

4. それぞれのインフラストラクチャ \\VMs\<VMName\> フォルダの内容を、対応する仮想マシン (VM) にコピーします。 （リモート スクリプトを使用している場合は、コンテンツが自動的に対象のVMにコピーされます。）続いて、次の Windows PowerShell スクリプトを管理者として実行します。

    > [!NOTE]
    > リモートで実行している既存のサーバーを修復する場合は、すべてのサーバーに対してファイル コピー処理が実行されるように、-ForcePushLBDScripts の切り替えを指定します。

    ```powershell
    # Install prereq software on the VMs.
    
    # If remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml

    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

5. 再起動を求めるメッセージが表示されるたびにコンピューターを再起動してください。 すべての前提条件がインストールされるまでは、再起動後に **.\\Configure-PreReqs.ps1** スクリプトを必ず再実行してください。 リモート処理の場合、すべてのコンピューターがオンラインに戻った際に **AllVMs** スクリプトを再実行します。
6. リモート処理スクリプトを使用する場合は、現在のユーザーが Microsoft Windows インストーラー パッケージ ファイル (.msiファイル) の共有フォルダにアクセスできることを確認してください。
7. リモート処理スクリプトを使用する場合は、ユーザーが **AOSNodeType**、**MRType**、**ReportServerType** タイプのコンピューターにアクセスしていないことを確認してください。 この条件に当てはまる場合は、ユーザーがログインしている理由によって、リモートスクリプトがコンピューターを再起動できなくなります。
8. VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。

    ```powershell
    # If remoting, execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    
    .\Complete-PreReqs.ps1
    ```

9. **Complete-PreReqs.ps1** の実行中にエラーが発生する場合、gMSA アカウントの更新が必要な場合があります。 インフラストラクチャ スクリプト フォルダから次のスクリプトを実行します。

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

12. 次のスクリプトを実行して VM のセットアップを検証します。

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    
    .\Test-D365FOConfiguration.ps1 
    ```

13. 続行する前に、検証スクリプトの一環として失敗する箇所を修正してください。
14. Service Fabric Explorer で、**クラスター** を選択し、Microsoft Service Fabric Cluster のバージョン (例: **8.2.1686.XXXX**) をメモします。
15. いずれかのオーケストレータノード ノードで、ファイル エクスプローラーを開きます。 **表示** タブの、**表示/非表示** グループで、**ファイル名の拡張子** と **非表示項目** の各チェック ボックスがオンになっていることを確認します。

    ![オプションを表示します。](media/bb83d249cdce333bdbb2e276ebce559c.png)

16. ドライブ C を展開し、次のフォルダにドリル ダウンします。 （パスの太字部分は、ノード名と設定によって異なることに注意してください）

    C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**

    このフォルダーには、Service Fabric のさまざまなバージョンのフォルダがリスト表示されます。 

17. 前述の手順でメモした Microsoft Service Fabric Cluster のバージョンと同じ名前のフォルダーを開きます。 
18. フォルダ内に .cab ファイルが表示されています。
19. .Cab ファイルを C:\\Temp にコピーし、コピーしたファイルを **MicrosoftAzureServiceFabric.cab** に変更します。 （Temp フォルダーがない場合は作成してください）
20. Windows PowerShell のコマンドプロンプトを管理者として開きます。
21. 次のコマンドを実行して、Service Fabric Cluster に接続します。 （必要に応じてコマンドを編集します）

    ```powershell
    #Connect to the Service Fabric Cluster. 
    Connect-ServiceFabricCluster 
    ```

22. 次のコマンドを実行して、ノードを追加し直します。 実行前に、**NodeName**、**IPAddress**、**UpgradeDomain**、**FaultDomain** パラメータに対して必要な編集を行ってください。 （既存のサーバーを置き換えている場合は、元の値をメモしておく必要があります）

    ```powershell
    Add-ServiceFabricNode -NodeName "AOS4" -NodeType "AOSNodeType" -IpAddressOrFQDN "10.0.0.19" -UpgradeDomain "ud0" -FaultDomain "fd:/fd0" -FabricRuntimePackagePath "C:\Temp\MicrosoftAzureServiceFabric.cab"
    ```

23. ノードを再追加した後は、Service Fabric エクスプローラーに戻り、アプリケーションの展開の状態を確認します。 すべての復元された AOS アプリケーション（**AXBootstrapperAppType**、**AXSFType**、**RTGatewayAppType**、**LBDTelemetryType-<envname\>** 、**MonitoringAgentAppType**）がプッシュ アウトされ、ノードにインストールされるには数分を要します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
