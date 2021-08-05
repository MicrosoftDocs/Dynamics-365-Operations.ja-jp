---
title: AOS ノードの削除と再インストール、または追加
description: このトピックでは、オンプレミス環境の アプリケーション オブジェクト サーバー (AOS) ノードを削除して、障害が発生したノードの削減または交換をする方法について説明します。
author: ttreen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Platform update 34
ms.openlocfilehash: cd566c9a30b5c90785c3ac67a52e3ea80e45b91d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351700"
---
# <a name="remove-and-reinstall-or-add-an-aos-node"></a>AOS ノードの削除と再インストール、または追加

[!include[banner](../includes/banner.md)]

このトピックでは、オンプレミス環境の アプリケーション オブジェクト サーバー (AOS) ノードを削除して、障害が発生したノードの削減または交換をする方法について説明します。 また、スケール アウト パフォーマンスの新しい AOS ノードを追加する方法についても説明します。

## <a name="remove-a-node"></a>ノードの削除

### <a name="option-1-use-a-configuration-file-preferred-option"></a>オプション 1：構成ファイルを使用する (推奨オプション)

**参照ドキュメント：**[Windows Server で実行されているスタンドアローンの Service Fabric Cluster へのノードの追加または削除](/azure/service-fabric/service-fabric-cluster-windows-server-add-remove-nodes)

1. Service Fabric エクスプローラー で、**クラスター** を選択し、Microsoft Service Fabric Cluster のバージョンをメモします。 この例では、クラスター バージョンが **6.5.676.9590** となっています。

    ![クラスター バージョン。](media/fe0c857aefd3a1174df38f8e0c644667.png)

2. いずれかのオーケストレータノード ノードで、ファイル エクスプローラーを開きます。 **表示** タブの、**表示/非表示** グループで、**ファイル名の拡張子** と **非表示項目** の各チェック ボックスがオンになっていることを確認します。

    ![オプションを表示します。](media/bb83d249cdce333bdbb2e276ebce559c.png)

3. ドライブ C を展開し、次のフォルダにドリル ダウンします。 （パスの太字部分は、ノード名と設定によって異なることに注意してください）

    C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**

    このフォルダーには、Microsoft Service Fabric のさまざまなバージョンのフォルダがリスト表示されます。 次に例を示します。

    ![131811633624852852 フォルダーのコンテンツ。](media/f843b5ceda67f767f54333851f5deeec.png)

5. 前述の手順でメモした Microsoft Service Fabric Cluster のバージョンと同じ名前のフォルダーを開きます。 この例では、フォルダの名称が **6.5.676.9590** となっています。
6. フォルダ内に .cab ファイルが表示されています。

    ![6.5.676.9590 フォルダーのコンテンツ。](media/fd04e00bc3d940f5637900e46db8f134.png)

7. .Cab ファイルを C:\\Temp にコピーし、コピーしたファイルを **MicrosoftAzureServiceFabric.cab** に変更します。 （Temp フォルダーがない場合は作成してください）

    ![Temp フォルダーにコピーされて名前変更されたファイル。](media/e146a300f030d0695be858d8c7261486.png)

8. Windows PowerShell のコマンドプロンプトを管理者として開きます。
9. 次のコマンドを実行して、Service Fabric Cluster に接続します。

    ```powershell
    #Connect to Service Fabric Cluster. Replace 123 with server/star thumbprint and use appropriate IP address
    Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123
    ```

    ![接続コマンドと結果。](media/0af2777b388b786d2ba6fe0b1f0f77dc.png)

10. 次のコマンドを実行して、構成ファイルを C:\\Temp\\ClusterConfig.json に保存します。 （C:\\Temp のパスが存在することを確認してください）

    ```powershell
    Get-ServiceFabricClusterConfiguration -UseApiVersion -ApiVersion 10-2017 >C:\Temp\ClusterConfig.json
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

    ![応答が停止したアップグレード。](media/c9a57cd8a5828a63a010d829eaab597c.png)

    クラスタ構成のアップグレード中に、**Add-ServiceFabricNode** コマンドを使用して既にノードが追加されているというエラーメッセージが表示された場合は、バージョン番号以外の構成ファイルを変更せずに構成のアップグレードを実行する必要があります。 この目的では、**Get-ServiceFabricClusterConfiguration** と **Start-ServiceFabricClusterConfigurationUpgrade** コマンドを使用することができます。

    ![バージョン番号以外の構成ファイルを変更せずに構成のアップグレードを実行します。](media/329b9c2bd807d7bca96e106037504e0e.png)

    また、 Service Fabric エクスプローラー で進行状況を確認することもできます。

    ![Service Fabric エクスプローラーの進捗情報。](media/99c6321f9da950d91a1709cae2473d97.png)

### <a name="option-2-use-service-fabric-explorer"></a>オプション 2：Service Fabric エクスプローラー の使用

1. Service Fabric エクスプローラーにログインします。
2. **設定** ボタン (歯車記号) を選択し、**詳細** モードがオンになっていることを確認します。

    ![詳細モードがオンになっています。](media/bc25caaed54da595a3c75429faaf73cb.png)

3. **ノード** を展開し、省略記号（**...**）ボタンをクリックし、**非アクティブ化（データの削除）** を選択します。 このオプションは、ノードがすでにダウンしている場合 (ノード サーバーが起動できない場合など) には使用できないことに注意してください。

    ![無効化 (データの削除) コマンド。](media/6865310acd6150cc81ee4a56aaeeed3f.png)

4. 無効化の確認が求められた際は、ノードの名前を入力し、**非アクティブ化（データの削除）** を選択します。

    ![ノードの無効化の確認。](media/49486a44d04b7a91431f18beebda43e8.png)

    ノードが非アクティブ化されると、状態が **無効** と表示されます。

    ![無効な状態のノード。](media/4dba61b4c22966cb4098cf832a4e5e90.png)

5. サーバーがまだ有効でドメインに接続されている場合、無効化されたノードを新しいサーバーに置き換える場合は、以下の手順を実行することが必要な場合があります。

    1. サーバーにサイン インします。
    2. ドメインからサーバーを削除します。
    3. サーバー名を変更します。
    4. IP アドレスを書き留めてから、IP アドレスを範囲内の空いているアドレスに変更します。
    5. サーバーをシャットダウンします。

6. サーバーのシャットダウンの完了後、または既にダウンしていた場合は、Service Fabric エクスプローラーの状態が反映されます。 省略符号（**...**）ボタンを再度クリックし、**ノードの状態を削除する** を選択します。

    ![ノードの状態を削除するコマンド。](media/e0460a280693cdf13896731aa7f2377f.png)

7. ノードを削除することを確認します。

    ![ノードの削除を確認。](media/a711e04b14b8adddc5d3941f010b32e0.png)

    ノードが削除されると、状態が **無効** と表示されます。

    ![無効な状態のノード。](media/c3f8dc79d51e535074e89dfca04006b8.png)

8. ノードの名前とタイプをメモします。 この例では、ノード名は **AOS1** で、タイプは **AOSNodeType** です。 ノード名がネットワーク名と一致しない可能性があることに注意してください。 また、**ドメインのアップグレード** と **障害ドメイン** の設定、およびIPアドレスについてもメモしておきます。 上記の図にはこれらの値がすべて表示されています。

## <a name="add-a-node"></a>ノードの追加

次の手順では、新しい AOS サーバーを起動します。

1. 削除された既存のサーバーを置き換える場合は、次の手順に従います：

    1. 以前の AOS サーバーのネットワーク名をサーバーに設定します。
    2. 元の IP アドレスを割り当てます。 この例では、IP アドレスを **10.0.0.9** としています。
    3. サーバーをドメインに追加します。

2. 既存のクラスターに新しいサーバーを追加する場合は、ConfigTemplate .xml ファイルを更新することで追加情報を含めることができます。 この情報は、前提条件を押し出して、Windows PowerShell スクリプトを使用して設定を適用する際に使用されます。
3. AOS サーバーのローカル管理者グループに **AXServiceUser** と **svc-AXSF\$** グループのマネージド サービス アカウント (gMSA) が追加されていることを確認してください。

    サーバーをドメインに接続した後は、[オンプレミス環境 (プラットフォーム更新プログラム 12 以降) の設定と展開](./setup-deploy-on-premises-pu12.md#follow-these-steps-for-each-vm-or-use-remoting-from-a-single-machine) に記載されているオンプレミス環境の前提条件に従う必要があります。 次の手順は、これら前提条件の手順をまとめたものです。

4. それぞれのインフラストラクチャ \\VMs\<VMName\> フォルダの内容を、対応する仮想マシン (VM) にコピーします。 （リモート スクリプトを使用している場合は、コンテンツが自動的に対象のVMにコピーされます。）続いて、次の Windows PowerShell スクリプトを管理者として実行します。

    > [!NOTE]
    > リモートで実行している既存のサーバーを修復する場合は、すべてのサーバーに対してファイルコピー処理が実行されるように、[インフラストラクチャ] フォルダから lbdscripts_remote_status.json ファイルを削除する必要があります。

    ```powershell
    # Install pre-req software on the VMs.
    # If Remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml
    .\Configure-PreReqs.ps1 -MSIFilePath <share folder path of the MSIs>
    ```

5. 再起動を求めるメッセージが表示されるたびにコンピューターを再起動してください。 すべての前提条件がインストールされるまでは、再起動後に **.\\Configure-PreReqs.ps1** スクリプトを必ず再実行してください。 リモート処理の場合、すべてのコンピューターがオンラインに戻った際に **AllVMs** スクリプトを再実行します。
6. リモート処理スクリプトを使用する場合は、現在のユーザーが Microsoft Windows インストーラー パッケージ ファイル (.msiファイル) の共有フォルダにアクセスできることを確認してください。
7. リモート処理スクリプトを使用する場合は、ユーザーが **AOSNodeType**、**MRType**、**ReportServerType** タイプのコンピューターにアクセスしていないことを確認してください。 この条件に当てはまる場合は、ユーザーがログインしている理由によって、リモートスクリプトがコンピューターを再起動できなくなります。
8. VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。

    ```powershell
    # If Remoting, only execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

9. **Add-GMSAonVM.ps1** の実行中にエラーが発生した場合は、次のコマンドを実行する必要があります。 （サービスア カウントが異なる場合は、このコマンドを編集してください。 ドル記号 \[\$\] をサービスアカウント名から削除することを忘れないでください。）

    ```powershell
    Get-ADServiceAccount -Identity svc-AXSF -properties PrincipalsAllowedToRetrieveManagedPassword
    ```

    ![Get コマンドと結果。](media/525f31b6281e87fd58075f2101f75118.png)

    **svc-AXFS\$** gMSA のパスワードを取得するにあたって、アクセス許可が与えられているサーバーの一覧が表示されます。 削除されたサーバーのグローバル一意識別子 (GUID) 値が表示される場合は、無視します。

10. 結果からプリンシパルの一覧をコピーし、それを使用して次のコマンドを編集または修正します。 （**Set** コマンドは付加されないため、すべての参照に再度追加する必要があります）

    ```powershell
    Set-ADServiceAccount -Identity svc-AXSF -PrincipalsAllowedToRetrieveManagedPassword  "CN=AOS1,CN=Computers,DC=contoso,DC=com","CN=AOS2,CN=Computers,DC=contoso,DC=com","CN=AOS3,CN=Computers,DC=contoso,DC=com"
    ```

    ![Set コマンド。](media/ff652391b87c72cacd318b588758e4fc.png)

11. 元 **Get** コマンドを実行して、新たな AOS ノードが再度追加されたことを確認します。 （この後の例では、AOS1 が PrincipalsAllowedToRetrieveManagedPassword の一覧に追加されていることが確認できます）

    ![元の Get コマンドと結果。](media/17b9c379b6328ed506d16270280146f4.png)

12. 次のスクリプトを実行して VM のセットアップを検証します。

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    .\Test-D365FOConfiguration.ps1
    ```

13. 続行する前に、検証スクリプトの一環として失敗する箇所を修正してください。
14. Service Fabric エクスプローラー で、**クラスター** を選択し、Microsoft Service Fabric Cluster のバージョンをメモします。 この例では、クラスター バージョンが **6.5.676.9590** となっています。

    ![クラスター バージョン。](media/fe0c857aefd3a1174df38f8e0c644667.png)

15. いずれかのオーケストレータノード ノードで、ファイル エクスプローラーを開きます。 **表示** タブの、**表示/非表示** グループで、**ファイル名の拡張子** と **非表示項目** の各チェック ボックスがオンになっていることを確認します。

    ![オプションを表示します。](media/bb83d249cdce333bdbb2e276ebce559c.png)

16. ドライブ C を展開し、次のフォルダにドリル ダウンします。 （パスの太字部分は、ノード名と設定によって異なることに注意してください）

    C:\\ProgramData\\SF\\**ORCH1**\\Fabric\\work\\Applications\\\_\_FabricSystem\\ **_App4294967295**\\work\\Store\\**131811633624852852**

    このフォルダーには、Service Fabric のさまざまなバージョンのフォルダがリスト表示されます。 次に例を示します。

    ![131811633624852852 フォルダーのコンテンツ。](media/f843b5ceda67f767f54333851f5deeec.png)

17. 前述の手順でメモした Microsoft Service Fabric Cluster のバージョンと同じ名前のフォルダーを開きます。 この例では、フォルダの名称が **6.5.676.9590** となっています。
18. フォルダ内に .cab ファイルが表示されています。

    ![6.5.676.9590 フォルダーのコンテンツ。](media/fd04e00bc3d940f5637900e46db8f134.png)

19. .Cab ファイルを C:\\Temp にコピーし、コピーしたファイルを **MicrosoftAzureServiceFabric.cab** に変更します。 （Temp フォルダーがない場合は作成してください）

    ![Temp フォルダーにコピーされて名前変更されたファイル。](media/e146a300f030d0695be858d8c7261486.png)

20. Windows PowerShell のコマンドプロンプトを管理者として開きます。
21. 次のコマンドを実行して、Service Fabric Cluster に接続します。 （必要に応じてコマンドを編集します）

    ```powershell
    #Connect to Service Fabric Cluster. Replace 123 with server/star thumbprint and use appropriate IP address
    Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123
    ```

    ![接続コマンドと結果。](media/0af2777b388b786d2ba6fe0b1f0f77dc.png)

22. 次のコマンドを実行して、ノードを追加し直します。 実行前に、**NodeName**、**IPAddress**、**UpgradeDomain**、**FaultDomain** パラメータに対して必要な編集を行ってください。 （既存のサーバーを置き換えている場合は、元の値をメモしておく必要があります）

    ```powershell
    Add-ServiceFabricNode -NodeName "AOS1" -NodeType "AOSNodeType" -IpAddressOrFQDN "10.0.0.9" -UpgradeDomain "ud0" -FaultDomain "fd:/fd0" -FabricRuntimePackagePath "C:\Temp\MicrosoftAzureServiceFabric.cab"
    ```

    ![コマンドと結果を追加します。](media/e8c153c1b8aa06af684a307f443c9b7b.png)

23. ノードを再追加した後は、Service Fabric エクスプローラーに戻り、アプリケーションの展開の状態を確認します。 すべての復元された AOS アプリケーション（**AXBootstrapperAppType**、**AXSFType**、**RTGatewayAppType**、**LBDTelemetryType-<envname\>** 、**MonitoringAgentAppType**）がプッシュ アウトされ、ノードにインストールされるには数分を要します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
