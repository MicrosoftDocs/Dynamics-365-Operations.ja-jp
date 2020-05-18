---
title: 証明書のローテーション
description: このトピックでは、既存の証明書を置く方法と、新しい証明書を使用するために環境内の参照を更新する方法について説明します。
author: PeterRFriis
manager: AnnBe
ms.date: 04/30/2020
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
ms.openlocfilehash: 6f1f6d8701eee44a7e8614fb804ccc0f14ced567
ms.sourcegitcommit: 821a54851a36ab735b3aca5114baff3b11aafe49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324533"
---
# <a name="certificate-rotation"></a><span data-ttu-id="7c842-103">証明書のローテーション</span><span class="sxs-lookup"><span data-stu-id="7c842-103">Certificate rotation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7c842-104">有効期限が近づくにつれて、Dynamics 365 Finance + Operations (オンプレミス) 環境で使用する証明書を回転することが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-104">You may need to rotate the certificates used by your Dynamics 365 Finance + Operations (on-premises) environment as they approach their expiration date.</span></span> <span data-ttu-id="7c842-105">このトピックでは、既存の証明書を置換する方法と、新しい証明書を使用するために環境内の参照を更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7c842-105">In this topic, you will learn how to replace the existing certificates and update the references within the environment to use the new certificates.</span></span>

> [!WARNING]
> <span data-ttu-id="7c842-106">証明書の有効期限が切れる前に、証明書ローテーションのプロセスを正しく開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-106">The certificate rotation process should be initiated well before the certificates expire.</span></span> <span data-ttu-id="7c842-107">これはデータ暗号化の証明書にとって非常に重要です。暗号化されたフィールドのデータが失われる可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="7c842-107">This is very important for the Data Encryption certificate, which could  cause data loss for encrypted fields.</span></span> <span data-ttu-id="7c842-108">詳細については、[証明書ローテーション後](#aftercertrotation)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c842-108">For more information, see [After certificate rotation](#aftercertrotation).</span></span> 
> 
> <span data-ttu-id="7c842-109">古い証明書は、証明書ローテーションプロセスが完了するまでそのままにしておく必要があり、事前に削除すると回転プロセスが失敗します。</span><span class="sxs-lookup"><span data-stu-id="7c842-109">Old certificates must remain in place until the certificate rotation process is complete, removing them in advance will cause the rotation process to fail.</span></span>

## <a name="preparation-steps"></a><span data-ttu-id="7c842-110">準備段階</span><span class="sxs-lookup"><span data-stu-id="7c842-110">Preparation steps</span></span> 

1. <span data-ttu-id="7c842-111">プロセス中に作成した元の**インフラストラクチャ**フォルダーの名前を変更して、[LCS からのセットアップスクリプトをダウンロード](setup-deploy-on-premises-pu12.md#downloadscripts)するようにします。</span><span class="sxs-lookup"><span data-stu-id="7c842-111">Rename the original **Infrastructure** folder that you created during the process to [Download setup scripts from LCS](setup-deploy-on-premises-pu12.md#downloadscripts).</span></span> <span data-ttu-id="7c842-112">フォルダーの名前を **InfrastructureOld** に変更します。</span><span class="sxs-lookup"><span data-stu-id="7c842-112">Rename the folder to **InfrastructureOld**.</span></span>

2. <span data-ttu-id="7c842-113">[LCS のダウンロード セットアップ スクリプト](setup-deploy-on-premises-pu12.md#downloadscripts)から最新のセットアップスクリプトをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7c842-113">Download the latest setup scripts from [Download setup scripts from LCS](setup-deploy-on-premises-pu12.md#downloadscripts).</span></span> <span data-ttu-id="7c842-114">**infrastructure** という名前のフォルダーにファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="7c842-114">Unzip the files into a folder that is named **Infrastructure**.</span></span>

3. <span data-ttu-id="7c842-115">**Configtemplate .Xml** および **clusterconfig. json** を **InfrastructureOld** から**インフラストラクチャ**にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7c842-115">Copy **ConfigTemplate.xml** and **ClusterConfig.json** from **InfrastructureOld** to **Infrastructure**.</span></span>

4. <span data-ttu-id="7c842-116">必要に応じて、**configtemplate.xml** で証明書をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7c842-116">Configure certificates as needed in **ConfigTemplate.xml**.</span></span> <span data-ttu-id="7c842-117">[証明書をコンフィギュレーションする](setup-deploy-on-premises-pu12.md#configurecert)の手順に従って、特に、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7c842-117">Follow the steps in [Configure certificates](setup-deploy-on-premises-pu12.md#configurecert), specifically these steps:</span></span>

    ```powershell
    # Create self-signed certs
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    
    # Export Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

5. <span data-ttu-id="7c842-118">[VM の設定](setup-deploy-on-premises-pu12.md#setupvms)に進みます。</span><span class="sxs-lookup"><span data-stu-id="7c842-118">Continue to [Setup VMs](setup-deploy-on-premises-pu12.md#setupvms).</span></span> <span data-ttu-id="7c842-119">このプロセスに必要な具体的な手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7c842-119">The specific steps that are needed for this process include:</span></span>

    1. <span data-ttu-id="7c842-120">各 VM で実行する必要があるスクリプトをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7c842-120">Export the scripts that must be run on each VM.</span></span>
    
        ```powershell
        # Export the script files to be executed on each VM into a directory VMs\<VMName>
        .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```

    2. <span data-ttu-id="7c842-121">各インフラストラクチャ\\VM<VMName>フォルダーのコンテンツを、対応する VM にコピーし (リモート処理スクリプトが使用されている場合は、コンテンツをターゲット VM に自動的にコピーします)、存在する場合は次のスクリプトを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="7c842-121">Copy the contents of each infrastructure\\VMs<VMName> folder into the corresponding VM (if remoting scripts are used, they will automatically copy the content to the target VMs), and then run the following scripts, if they exist.</span></span> <span data-ttu-id="7c842-122">これらの手順を管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="7c842-122">Perform these steps as an Administrator.</span></span>
    
        ```powershell
        # If remoting, only execute
        # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ForcePushLBDScripts

        .\Import-PfxFiles.ps1
        .\Set-CertificateAcls.ps1
        ```
        
    3. <span data-ttu-id="7c842-123">次のスクリプトを実行して VM のセットアップを検証します。</span><span class="sxs-lookup"><span data-stu-id="7c842-123">Run the following script to validate the VM setup.</span></span>
    
        ```powershell
        # If remoting, only execute
        # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        .\Test-D365FOConfiguration.ps1
        ```

6. <span data-ttu-id="7c842-124">Axdataenciphermentcert 証明書がローテーションされている場合は、資格情報の .json ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-124">If axdataenciphermentcert certificates are rotated, you need to regenerate the credentials.json file.</span></span> <span data-ttu-id="7c842-125">詳細については、「[資格情報の暗号化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#encryptcred)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c842-125">For more information, see [Encrypt credentials](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#encryptcred).</span></span>

7. <span data-ttu-id="7c842-126">後で LCS で使用できる値を保持するには、次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7c842-126">Run the following PowerShell command to have values that can be used in LCS later.</span></span> <span data-ttu-id="7c842-127">詳細については、[LCS からのオンプレミス環境の配置](setup-deploy-on-premises-pu12.md#deploy) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c842-127">For more information, see [Deploy your on-premises environment from LCS](setup-deploy-on-premises-pu12.md#deploy).</span></span>

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```


## <a name="activate-new-certificates-within-service-fabric-cluster"></a><span data-ttu-id="7c842-128">Service Fabric cluster 内での新しい証明書のアクティブ化</span><span class="sxs-lookup"><span data-stu-id="7c842-128">Activate new certificates within Service Fabric cluster</span></span>

### <a name="service-fabric-with-certificates-that-are-not-expired"></a><span data-ttu-id="7c842-129">期限切れになっていない証明書を含む Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7c842-129">Service Fabric with certificates that are not expired</span></span>

1. <span data-ttu-id="7c842-130">Clusterconfig.json ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="7c842-130">Edit the Clusterconfig.json file.</span></span> <span data-ttu-id="7c842-131">ファイル内の次のセクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="7c842-131">Find the following section in the file.</span></span>  
    ```json
    "security": {
        "metadata":  "The Credential type X509 indicates this is cluster is secured using X509 Certificates. The thumbprint format is - d5 ec 42 3b 79 cb e5 07 fd 83 59 3c 56 b9 d5 31 24 25 42 64.",
        "ClusterCredentialType":  "X509",
        "ServerCredentialType":  "X509",
        "CertificateInformation":  {
            "ClusterCertificate":  {
                                       "X509StoreName":  "My",
                                        "Thumbprint": "*Old server thumbprint(Star/SF)*"
                                   },
            "ServerCertificate":   {
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

2. <span data-ttu-id="7c842-132">ファイルのそのセクションを、次のセクションと置換します。</span><span class="sxs-lookup"><span data-stu-id="7c842-132">Replace that section in the file with following section.</span></span>

    ```json
    "security":  {
        "metadata":  "The Credential type X509 indicates this is cluster is secured using X509 Certificates. The thumbprint format is - d5 ec 42 3b 79 cb e5 07 fd 83 59 3c 56 b9 d5 31 24 25 42 64.",
        "ClusterCredentialType":  "X509",
        "ServerCredentialType":  "X509",
        "CertificateInformation":  {
                                        "ClusterCertificate":  {
                                                                    "X509StoreName":  "My",
                                                                    "Thumbprint":  "New server thumbprint(Star/SF)"
                                                                    ,"ThumbprintSecondary": "Old server thumbprint(Star/SF)"
                                                               },
                                        "ServerCertificate":   {
                                                                    "X509StoreName":  "My",
                                                                    "Thumbprint":  "New server thumbprint(Star/SF)"
                                                                    ,"ThumbprintSecondary":"Old server thumbprint(Star/SF)"
                                                               },
                                        "ClientCertificateThumbprints":  [
                                                                                                                                                                                           {
                                                                                "CertificateThumbprint":  "Old client thumbprint",
                                                                                "IsAdmin":  false
                                                                            },
                                                                            {
                                                                                "CertificateThumbprint":  "New client thumbprint",
                                                                                "IsAdmin":  true
                                                                            }
                                                                          ]
                                       }
                    },
    ```

3. <span data-ttu-id="7c842-133">新しいサムプリントと古いサムプリント値を編集します。</span><span class="sxs-lookup"><span data-stu-id="7c842-133">Edit the new and old thumbprint values.</span></span> 

4. <span data-ttu-id="7c842-134">2.0.0 などの clusterConfigurationVersion を新しいバージョンに変更します。</span><span class="sxs-lookup"><span data-stu-id="7c842-134">Change clusterConfigurationVersion to the new version, for example 2.0.0.</span></span>

    ```json
    {
    "name": "Dynamics365Operations",
    "clusterConfigurationVersion": "2.0.0",
    "apiVersion": "10-2017",
    ```
    
5. <span data-ttu-id="7c842-135">Clusterconfig.json ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="7c842-135">Save the new ClusterConfig.json file.</span></span>

6. <span data-ttu-id="7c842-136">次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7c842-136">Run the following PowerShell command.</span></span>

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

### <a name="service-fabric-with-or-without-expired-certificates-cluster-not-accessible"></a><span data-ttu-id="7c842-137">期限が切れた証明書 (クラスターにアクセスできない)を含むまたは含まないサービスファブリック</span><span class="sxs-lookup"><span data-stu-id="7c842-137">Service Fabric with or without expired certificates (cluster not accessible)</span></span>

<span data-ttu-id="7c842-138">このプロセスを続行するには、 [オンプレミスの展開のトラブルシューティング](troubleshoot-on-prem.md#clean-up-an-existing-environment-and-redeploy) を行ってください。</span><span class="sxs-lookup"><span data-stu-id="7c842-138">Continue this process following [Troubleshoot on-premises deployments](troubleshoot-on-prem.md#clean-up-an-existing-environment-and-redeploy).</span></span>

## <a name="localagent-certificate-update-if-needed"></a><span data-ttu-id="7c842-139">LocalAgent 証明書の更新 (必要な場合)</span><span class="sxs-lookup"><span data-stu-id="7c842-139">LocalAgent certificate update (if needed)</span></span>

1. <span data-ttu-id="7c842-140">いずれかの Orchestrator ノードに対して次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7c842-140">Run the following PowerShell command on one of the Orchestrator nodes.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. <span data-ttu-id="7c842-141">次の PowerShell コマンドを実行して、新しい LocalAgent の拇印を記録します。</span><span class="sxs-lookup"><span data-stu-id="7c842-141">Run the following PowerShell command and note the new LocalAgent thumbprint.</span></span>

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

3. <span data-ttu-id="7c842-142">「[テナント向けの LCS 接続コンフィギュレーション](setup-deploy-on-premises-pu12.md#configurelcs)」の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="7c842-142">Follow the steps in [Configure LCS connectivity for the tenant](setup-deploy-on-premises-pu12.md#configurelcs).</span></span>

    > [!NOTE] 
    > <span data-ttu-id="7c842-143">**KeyId 『\<key\>』による既存の資格情報の更新は許可されていません**というエラーメッセージを受信した場合は、[エラーメッセージ 「KeyId 『<key>』を含む既存の資格情報の更新は許可されていません」](troubleshoot-on-prem.md#error-updates-to-existing-credential-with-keyid-key-is-not-allowed)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="7c842-143">If you receive the error **Update to existing credential with KeyId '\<key\>' is not allowed**, follow the instructions in [Error: "Updates to existing credential with KeyId '<key>' is not allowed"](troubleshoot-on-prem.md#error-updates-to-existing-credential-with-keyid-key-is-not-allowed).</span></span>

4. <span data-ttu-id="7c842-144">[コネクタのコンフィギュレーションを続行し、オンプレミスのローカルエージェントをインストールします。](setup-deploy-on-premises-pu12.md#configureconnector)具体的には、次の変更があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-144">Continue with [Configure a connector and install an on-premises local agent](setup-deploy-on-premises-pu12.md#configureconnector), specifically the following changes:</span></span>

    - <span data-ttu-id="7c842-145">クライアント証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="7c842-145">Client certificate thumbprint</span></span>
    - <span data-ttu-id="7c842-146">サーバー証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="7c842-146">Server certificate thumbprint</span></span>
    - <span data-ttu-id="7c842-147">テナント サービス プリンシパル証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="7c842-147">Tenant service principle certificate thumbprint</span></span>

## <a name="update-deployment-settings-in-lcs"></a><span data-ttu-id="7c842-148">LCS の展開設定の更新</span><span class="sxs-lookup"><span data-stu-id="7c842-148">Update deployment settings in LCS</span></span>

> [!NOTE]
>  <span data-ttu-id="7c842-149">ただし、クライアント、データ署名、および暗号化証明書は置換のみ行われます。</span><span class="sxs-lookup"><span data-stu-id="7c842-149">Note that the Client, Data Signing, and Encipherment certificates will only be replaced.</span></span> <span data-ttu-id="7c842-150">また、「[資格情報の暗号化](setup-deploy-on-premises-pu12.md#encryptcred)」で説明されているように、資格情報の Credentials.json ファイルを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-150">You will also need to recreate the Credentials.json file, as described in [Encrypt credentials](setup-deploy-on-premises-pu12.md#encryptcred).</span></span>
>
> <span data-ttu-id="7c842-151">続行する前に、ロケール Dynamics データベースのバックアップを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-151">Before you continue, you need to make a backup of the local Dynamics database.</span></span>

1. <span data-ttu-id="7c842-152">LCS で、証明書の変更を希望する環境についての「完全な詳細情報」リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7c842-152">In LCS, select the "Full Details" link for the environment where you want to change the certificates.</span></span>

2. <span data-ttu-id="7c842-153">**管理** を選択し、**更新の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c842-153">Select **Maintain** and then select **Update Settings**.</span></span>

    ![更新設定の適用](media/addf4f1d0c0a86d840a6a412f774e474.png)

3. <span data-ttu-id="7c842-155">拇印を、以前にコンフィギュレーションした新しい拇印に変更します (これらの属性は、InfrastructureScripts フォルダの ConfigTemplate.xml ファイルを確認してください)。</span><span class="sxs-lookup"><span data-stu-id="7c842-155">Change the thumbprints to the new ones that you have previously configured (you can find these in the ConfigTemplate.xml file in the InfrastructureScripts folder).</span></span>

    ![配置設定の拇印](media/07da4d7e02f11878ee91c61b4f561a50.png)

    ![配置設定の拇印](media/785caaf4ee652d66c0d88cf615a57e26.png)

4. <span data-ttu-id="7c842-158">**準備**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c842-158">Select **Prepare**.</span></span>

5. <span data-ttu-id="7c842-159">ダウンロードおよび準備が完了すると、**環境の更新** ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c842-159">After downloading and preparation is complete, the **Update environment** button will display.</span></span>

    ![環境の更新ボタン](media/0a9d43044593450f1a828c0dd7698024.png)

6. <span data-ttu-id="7c842-161">**環境の更新**を選択して、環境の更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="7c842-161">Select **Update environment** to start updating your environment.</span></span>

7. <span data-ttu-id="7c842-162">更新中、環境は使用できません。</span><span class="sxs-lookup"><span data-stu-id="7c842-162">During the update, the environment will be unavailable.</span></span>

8. <span data-ttu-id="7c842-163">新しい証明書を使用して環境を正常に更新した後、エクスプローラー Service Fabric Clusterで新しい拇印を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7c842-163">After the environment is successfully updated with the new certificates, you can check the new thumbprints in Service Fabric Cluster Explorer.</span></span> <span data-ttu-id="7c842-164">サービス Fabric Explorer からの拇印名の名前は、Lifecycle Services 内の拇印の名前とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-164">Note that the name of the thumbprint name from Service Fabric Explorer might differ from the names of the thumbprints that are in Lifecycle Services.</span></span> <span data-ttu-id="7c842-165">違いがあっても、値は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-165">Despite the differences, the values should be the same.</span></span>

    <span data-ttu-id="7c842-166">次の例では、同じ拇印の名前がいくらか異なっている例の一部です。</span><span class="sxs-lookup"><span data-stu-id="7c842-166">Here is an example of how the name of the same thumbprint might differ.</span></span>

    ![配置設定の拇印の例](media/038173714b2fb6cf12acc4bda2a3dde5.png)

    ![配置設定の拇印の例](media/642f6434da9cdeac3651b765acca08fa.png)

## <a name="update-other-certificates-as-needed"></a><span data-ttu-id="7c842-169">必要に応じて他の証明書を更新する</span><span class="sxs-lookup"><span data-stu-id="7c842-169">Update other certificates as needed</span></span>

1. <span data-ttu-id="7c842-170">SQL server 証明書の有効期限が切れていないかどうかを常に確認してください。</span><span class="sxs-lookup"><span data-stu-id="7c842-170">Always check if the SQL server certificate has expired.</span></span> <span data-ttu-id="7c842-171">詳細については、「[SQL Server の設定](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#setupsql)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c842-171">For more information, see [Set up SQL Server](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#setupsql).</span></span>

2. <span data-ttu-id="7c842-172">Active Directory フェデレーション サービス (ADFS) 証明書の有効期限が切れていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7c842-172">Check to be sure that the Active Directory Federation Service (ADFS) certificate has not expired.</span></span>

## <a name="after-certificate-rotation"></a><a name="aftercertrotation"></a><span data-ttu-id="7c842-173">証明書ローテーション後</span><span class="sxs-lookup"><span data-stu-id="7c842-173">After certificate rotation</span></span>

### <a name="data-encryption-certificate"></a><span data-ttu-id="7c842-174">データの暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="7c842-174">Data encryption certificate</span></span>

<span data-ttu-id="7c842-175">この証明書は、データベースに格納されているデータを暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c842-175">This certificate is used to encrypt data stored in the database.</span></span> <span data-ttu-id="7c842-176">既定では、この証明書を使用して暗号化される特定のフィールドがあります。これらのフィールドは、[ここ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/database/dbmovement-scenario-goldenconfig#document-the-values-of-encrypted-fields)でオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="7c842-176">By default there are certain fields that are encrypted with this certificate, you can check those fields [here](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/database/dbmovement-scenario-goldenconfig#document-the-values-of-encrypted-fields).</span></span> <span data-ttu-id="7c842-177">ただし、この API を使用して、ユーザーが暗号化すべきと判断した他のフィールドを暗号化することができます。</span><span class="sxs-lookup"><span data-stu-id="7c842-177">However, our API can be used to encrypt other fields that customers deem should be encrypted.</span></span> 

<span data-ttu-id="7c842-178">プラットフォーム更新 33 からは、「データ暗号化証明書をローテーションする場合は営業時間外に実行する必要がある、暗号化されたデータ ローテーション システム ジョブ」というタイトルのバッチ ジョブが、新しくローテーションされた証明書を使用してデータを再暗号化します。</span><span class="sxs-lookup"><span data-stu-id="7c842-178">Beginning with platform update 33, the batch job titled “Encrypted data rotation system job that needs to run at off hours when the data encryption certificate rotated” will re-encrypt data with the newly rotated certificate.</span></span> <span data-ttu-id="7c842-179">これは、2 時間から 3 日の間に実行されるクローラー バッチ ジョブで、暗号化されたすべてのデータを使用して新しい証明書を再暗号化します。</span><span class="sxs-lookup"><span data-stu-id="7c842-179">This is a crawler batch job that will run between 2 hours to 3 days to re-encrypt the new certificate with all of the encrypted data.</span></span> <span data-ttu-id="7c842-180">データの量によっては、クローラーをノートよりも短い期間で完了できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-180">Depending on the amount of data, it's possible that the crawler is able to finish in less time than note.</span></span>

> [!WARNING]
> <span data-ttu-id="7c842-181">暗号化されたデータがすべて再暗号化され、期限が切れるまでは、古いデータ暗号化証明書が削除されなうようにしてください。</span><span class="sxs-lookup"><span data-stu-id="7c842-181">Make sure that the old Data Encryption certificate is not removed before all encrypted data has been re-encrypted and it has not expired.</span></span> <span data-ttu-id="7c842-182">そうしないと、これによってデータが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7c842-182">Otherwise, this could lead to data loss.</span></span>
