---
title: 証明書のローテーション
description: このトピックでは、既存の証明書を置く方法と、新しい証明書を使用するために環境内の参照を更新する方法について説明します。
author: PeterRFriis
manager: AnnBe
ms.date: 09/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: 08a0c34eb18d84a7a154f7bbab867301f113d16b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183407"
---
# <a name="certificate-rotation"></a>証明書のローテーション

[!include[banner](../includes/banner.md)]

有効期限が近づくにつれて、Dynamics 365 Finance + Operations (オンプレミス) 環境で使用する証明書を回転することが必要となる場合があります。 このトピックでは、既存の証明書を置換する方法と、新しい証明書を使用するために環境内の参照を更新する方法について説明します。

> [!NOTE]
> 古い証明書は、証明書ローテーションプロセスが完了するまでそのままにしておく必要があり、事前に削除すると回転プロセスが失敗します。

## <a name="preparation-steps"></a>準備段階 

1. プロセス中に作成した元の**インフラストラクチャ**フォルダーの名前を変更して、[LCS からのセットアップスクリプトをダウンロード](setup-deploy-on-premises-pu12.md#downloadscripts)するようにします。 フォルダーの名前を **InfrastructureOld** に変更します。

2. [LCS のダウンロード セットアップ スクリプト](setup-deploy-on-premises-pu12.md#downloadscripts)から最新のセットアップスクリプトをダウンロードします。 **infrastructure** という名前のフォルダーにファイルを解凍します。

3. **Configtemplate .Xml** および **clusterconfig. json** を **InfrastructureOld** から**インフラストラクチャ**にコピーします。

4. 必要に応じて、**configtemplate.xml** で証明書をコンフィギュレーションします。 [証明書をコンフィギュレーションする](setup-deploy-on-premises-pu12.md#configurecert)の手順に従って、特に、次の手順を実行します。

    ```powershell
    # Create self-signed certs
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    
    # Export Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

5. [VM の設定](setup-deploy-on-premises-pu12.md#setupvms)に進みます。 このプロセスに必要な具体的な手順は次のとおりです。

    1. 各 VM で実行する必要があるスクリプトをエクスポートします。
    
        ```powershell
        # Export the script files to be executed on each VM into a directory VMs\<VMName>
        .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```

    2. 各インフラストラクチャ\\VM<VMName>フォルダーのコンテンツを、対応する VM にコピーし (リモート処理スクリプトが使用されている場合は、コンテンツをターゲット VM に自動的にコピーします)、存在する場合は次のスクリプトを管理者として実行します。 これらの手順を管理者として実行します。
    
        ```powershell
        # If remoting, only execute
        # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

        .\Import-PfxFiles.ps1
        .\Set-CertificateAcls.ps1
        ```
        
    3. 次のスクリプトを実行して VM のセットアップを検証します。
    
        ```powershell
        .\Test-D365FOConfiguration.ps1
        ```

6. Axdataenciphermentcert 証明書がローテーションされている場合は、資格情報の .json ファイルを再生成する必要があります。 詳細については、「[資格情報の暗号化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#encryptcred)」を参照してください。

7. 後で LCS で使用できる値を保持するには、次の PowerShell コマンドを実行します。 詳細については、[LCS からのオンプレミス環境の配置](setup-deploy-on-premises-pu12.md#deploy) を参照してください。

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    `````


## <a name="activate-new-certificates-within-service-fabric-cluster"></a>Service Fabric Cluster 内での新しい証明書のアクティブ化

### <a name="service-fabric-with-certificates-that-are-not-expired"></a>期限切れになっていない証明書を含む Service Fabric

1. Clusterconfig.json ファイルを編集します。 ファイル内の次のセクションを検索します。  
    ```
                       "security":  {
                                        "metadata":  "The Credential type X509 indicates this is cluster is secured using X509 Certificates. The thumbprint format is - d5 ec 42 3b 79 cb e5 07 fd 83 59 3c 56 b9 d5 31 24 25 42 64.",
                                        "ClusterCredentialType":  "X509",
                                        "ServerCredentialType":  "X509",
                                        "CertificateInformation":  {
                                                                       "ClusterCertificate":  {
                                                                                                  "X509StoreName":  "My",
                                                                                                  "Thumbprint": "*Old server thumbprint(Star/SF)*"
                                                                                              },
                                                                       "ServerCertificate":  {
                                                                                                 "X509StoreName":  "My",
                                                 "Thumbprint": "*Old server thumbprint(Star/SF)*"
                                                                                             },
                                                                       "ClientCertificateThumbprints":  [
                                                                                                            {
                                                                                                                "CertificateThumbprint": "*Old client thumbprint*",
                                                                                                                "IsAdmin":  true
                                                                                                            }
                                                                                                        ]
                                                                   }
                                    },
    ```

2. ファイルのそのセクションを、次のセクションと置換します。

    ```
                       "security":  {
                                        "metadata":  "The Credential type X509 indicates this is cluster is secured using X509 Certificates. The thumbprint format is - d5 ec 42 3b 79 cb e5 07 fd 83 59 3c 56 b9 d5 31 24 25 42 64.",
                                        "ClusterCredentialType":  "X509",
                                        "ServerCredentialType":  "X509",
                                        "CertificateInformation":  {
                                                                       "ClusterCertificate":  {
                                                                                                  "X509StoreName":  "My",
                                                                                                  "Thumbprint":  "New Server humbprint(Star/SF)"
                                                 ,"ThumbprintSecondary": "Old Server humbprint(Star/SF)"
                                                                                              },
                                                                       "ServerCertificate":  {
                                                                                                 "X509StoreName":  "My",
                                                                                                 "Thumbprint":  "New Server humbprint(Star/SF)"
                                                 ,"ThumbprintSecondary":"Old Server humbprint(Star/SF)"
                                                                                             },
                                                                       "ClientCertificateThumbprints":  [
                                                                                                            {
                                                                                                                "CertificateThumbprint":  "Old Client Thumbprint",
                                                                                                                "IsAdmin":  false
                                                                                                            },
                                                                                                            {
                                                                                                                "CertificateThumbprint":  "New Client Thumbprint",
                                                                                                                "IsAdmin":  true
                                                                                                            }
                                                                                                        ]
                                                                   }
                                    },
    ```

3. 新しいサムプリントと古いサムプリント値を編集します。 

4. 2.0.0 などの clusterConfigurationVersion を新しいバージョンに変更します。

    ```
    {
    "name": "Dynamics365Operations",
    "clusterConfigurationVersion": "2.0.0",
    "apiVersion": "10-2017",
    ```
5. Clusterconfig.json ファイルを保存します。

6. 次の PowerShell コマンドを実行します。

    ```powershell
    # Connect to the Service Fabric cluster
    Connect-ServiceFabricCluster

    # Get path of ClusterConfig.json for following command
    # Note that after running the following command, you need to manually cancel using the red button (Stop Operation) in Windows PowerShell ISE or Ctrl+C in Windows PowerShell, otherwise you will receive the following notification, "Start-ServiceFabricClusterConfigurationUpgrade : Operation timed out.". Be aware that the upgrade will proceed.
    Start-ServiceFabricClusterConfigurationUpgrade -ClusterConfigPath ClusterConfig.json

    # If you are using a single Microsoft SQL Server Reporting Services node, use UpgradeReplicaSetCheckTimeout to skip PreUpgradeSafetyCheck check, otherwise it will timeout
    Update-ServiceFabricClusterUpgrade -UpgradeReplicaSetCheckTimeoutSec 30
    
    # To monitor the status of the upgrade, run the following and note UpgradeState and UpgradeReplicaSetCheckTimeout
    Get-ServiceFabricClusterUpgrade
    
    # While monitoring the status of the upgrade, if UpgradeReplicaSetCheckTimeout was reset to the default (example 49710.06:28:15), run the following command again
    Update-ServiceFabricClusterUpgrade -UpgradeReplicaSetCheckTimeoutSec 30
    
    # When UpgradeState shows RollingForwardCompleted, the upgrade is finished
    ```

### <a name="service-fabric-with-or-without-expired-certificates-cluster-not-accessible"></a>期限が切れた証明書 (クラスターにアクセスできない)を含むまたは含まないサービスファブリック

[既存の環境をクリーンアップして再配置する](troubleshoot-on-prem.md#clean-up-an-existing-environment-and-redeploy)まで、このプロセスを続行します。

## <a name="localagent-certificate-update-if-needed"></a>LocalAgent 証明書の更新 (必要な場合)

1. いずれかの Orchestrator ノードに対して次の PowerShell コマンドを実行します。

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. 次の PowerShell コマンドを実行して、新しい LocalAgent の拇印を記録します。

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

3. 「[テナント向けの LCS 接続コンフィギュレーション](setup-deploy-on-premises-pu12.md#configurelcs)」の手順に従ってください。

    > [!NOTE] 
    > **KeyId 『\<key\>』による既存の資格情報の更新は許可されていません**というエラーメッセージを受信した場合は、[エラーメッセージ 「KeyId 『<key>』を含む既存の資格情報の更新は許可されていません」](troubleshoot-on-prem.md#error-updates-to-existing-credential-with-keyid-key-is-not-allowed)に従ってください。

4. [コネクタのコンフィギュレーションを続行し、オンプレミスのローカルエージェントをインストールします。](setup-deploy-on-premises-pu12.md#configureconnector)具体的には、次の変更があります。

    - クライアント証明書の拇印
    - サーバー証明書の拇印
    - テナント サービス プリンシパル証明書の拇印

## <a name="update-deployment-settings-in-lcs"></a>LCS の展開設定の更新

> [!NOTE]
>  ただし、クライアント、データ署名、および暗号化証明書は置換のみ行われます。 また、「[資格情報の暗号化](setup-deploy-on-premises-pu12.md#encryptcred)」で説明されているように、資格情報の Credentials.json ファイルを再作成する必要があります。

> 続行する前に、ロケール Dynamics データベースのバックアップを作成する必要があります。

1. LCS で、証明書の変更を希望する環境についての「完全な詳細情報」リンクを選択します。

2. **管理** を選択し、**更新の設定** を選択します。

    !更新設定の適用[](media/addf4f1d0c0a86d840a6a412f774e474.png)

3. 拇印を、以前にコンフィギュレーションした新しい拇印に変更します (これらの属性は、InfrastructureScripts フォルダの ConfigTemplate.xml ファイルを確認してください)。

    ![配置設定の拇印](media/07da4d7e02f11878ee91c61b4f561a50.png)

    ![配置設定の拇印](media/785caaf4ee652d66c0d88cf615a57e26.png)

4. **準備**を選択します。

5. ダウンロードおよび準備が完了すると、**環境の更新** ボタンが表示されます。

    ![環境の更新ボタン](media/0a9d43044593450f1a828c0dd7698024.png)

6. **環境の更新**を選択して、環境の更新を開始します。

7. 更新中、環境は使用できません。

8. 新しい証明書を使用して環境を正常に更新した後、エクスプローラー Service Fabric Clusterで新しい拇印を確認できます。 サービス Fabric Explorer からの拇印名の名前は、Lifecycle Services 内の拇印の名前とは異なる場合があります。 違いがあっても、値は同じである必要があります。

    次の例では、同じ拇印の名前がいくらか異なっている例の一部です。

    ![配置設定の拇印の例](media/038173714b2fb6cf12acc4bda2a3dde5.png)

    ![配置設定の拇印の例](media/642f6434da9cdeac3651b765acca08fa.png)

## <a name="update-other-certificates-as-needed"></a>必要に応じて他の証明書を更新する

1. SQL server 証明書の有効期限が切れていないかどうかを常に確認してください。 詳細については、「[SQL Server の設定](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#setupsql)」を参照してください。

2. Active Directory フェデレーション サービス (ADFS) 証明書の有効期限が切れていないことを確認します。 
