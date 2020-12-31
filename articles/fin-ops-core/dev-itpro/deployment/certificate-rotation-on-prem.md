---
title: 証明書のローテーション
description: このトピックでは、既存の証明書を置く方法と、新しい証明書を使用するために環境内の参照を更新する方法について説明します。
author: PeterRFriis
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: 7b5e6b38aedb17850e0fe41cc81c182c2608dc78
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686345"
---
# <a name="certificate-rotation"></a><span data-ttu-id="fda5e-103">証明書のローテーション</span><span class="sxs-lookup"><span data-stu-id="fda5e-103">Certificate rotation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fda5e-104">有効期限が近づくにつれて、Dynamics 365 Finance + Operations (オンプレミス) 環境で使用する証明書を回転することが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-104">You may need to rotate the certificates used by your Dynamics 365 Finance + Operations (on-premises) environment as they approach their expiration date.</span></span> <span data-ttu-id="fda5e-105">このトピックでは、既存の証明書を置換する方法と、新しい証明書を使用するために環境内の参照を更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-105">In this topic, you will learn how to replace the existing certificates and update the references within the environment to use the new certificates.</span></span>

> [!WARNING]
> <span data-ttu-id="fda5e-106">証明書の有効期限が切れる前に、証明書ローテーションのプロセスを正しく開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-106">The certificate rotation process should be initiated well before the certificates expire.</span></span> <span data-ttu-id="fda5e-107">これはデータ暗号化の証明書にとって非常に重要です。暗号化されたフィールドのデータが失われる可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="fda5e-107">This is very important for the Data Encryption certificate, which could cause data loss for encrypted fields.</span></span> <span data-ttu-id="fda5e-108">詳細については、[証明書ローテーション後](#aftercertrotation)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-108">For more information, see [After certificate rotation](#aftercertrotation).</span></span> 
> 
> <span data-ttu-id="fda5e-109">古い証明書は、証明書ローテーションプロセスが完了するまでそのままにしておく必要があり、事前に削除すると回転プロセスが失敗します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-109">Old certificates must remain in place until the certificate rotation process is complete, removing them in advance will cause the rotation process to fail.</span></span>

> [!CAUTION]
> <span data-ttu-id="fda5e-110">この証明書ローテーション プロセスは、7.0.x および 7.1. x を実行する Service Fabric クラスターでは行わないでください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-110">The certificate rotation process should not be carried out on Service Fabric clusters running 7.0.x and 7.1.x.</span></span> 
>
> <span data-ttu-id="fda5e-111">証明書ローテーションをする前に Service Fabric Clusterを 7.2. x にアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="fda5e-111">Upgrade your Service Fabric cluster to 7.2.x before attempting certificate rotation.</span></span>

## <a name="preparation-steps"></a><span data-ttu-id="fda5e-112">準備段階</span><span class="sxs-lookup"><span data-stu-id="fda5e-112">Preparation steps</span></span> 

1. <span data-ttu-id="fda5e-113">プロセス中に作成した元の **インフラストラクチャ** フォルダーの名前を変更して、[LCS からのセットアップスクリプトをダウンロード](setup-deploy-on-premises-pu12.md#downloadscripts)するようにします。</span><span class="sxs-lookup"><span data-stu-id="fda5e-113">Rename the original **Infrastructure** folder that you created during the process to [Download setup scripts from LCS](setup-deploy-on-premises-pu12.md#downloadscripts).</span></span> <span data-ttu-id="fda5e-114">フォルダーの名前を **InfrastructureOld** に変更します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-114">Rename the folder to **InfrastructureOld**.</span></span>

2. <span data-ttu-id="fda5e-115">[LCS のダウンロード セットアップ スクリプト](setup-deploy-on-premises-pu12.md#downloadscripts)から最新のセットアップスクリプトをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="fda5e-115">Download the latest setup scripts from [Download setup scripts from LCS](setup-deploy-on-premises-pu12.md#downloadscripts).</span></span> <span data-ttu-id="fda5e-116">**infrastructure** という名前のフォルダーにファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-116">Unzip the files into a folder that is named **Infrastructure**.</span></span>

3. <span data-ttu-id="fda5e-117">**Configtemplate .Xml** および **clusterconfig. json** を **InfrastructureOld** から **インフラストラクチャ** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="fda5e-117">Copy **ConfigTemplate.xml** and **ClusterConfig.json** from **InfrastructureOld** to **Infrastructure**.</span></span>

4. <span data-ttu-id="fda5e-118">必要に応じて、**configtemplate.xml** で証明書をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="fda5e-118">Configure certificates as needed in **ConfigTemplate.xml**.</span></span> <span data-ttu-id="fda5e-119">[証明書をコンフィギュレーションする](setup-deploy-on-premises-pu12.md#configurecert)の手順に従って、特に、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-119">Follow the steps in [Configure certificates](setup-deploy-on-premises-pu12.md#configurecert), specifically these steps:</span></span>

    ```powershell
    # Create self-signed certs
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="fda5e-120">自己署名証明書は、実稼働環境では使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-120">Self-signed certificates should never be used in production environments.</span></span> <span data-ttu-id="fda5e-121">信頼できる証明書を使用している場合は、ConfigTemplate.xml ファイル内のこれらの証明書の値を手動で更新します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-121">If you're using trusted certificates, manually update the values of those certificates in the ConfigTemplate.xml file.</span></span>

    ```powershell
    # Export Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

5. <span data-ttu-id="fda5e-122">[VM の設定](setup-deploy-on-premises-pu12.md#setupvms)に進みます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-122">Continue to [Setup VMs](setup-deploy-on-premises-pu12.md#setupvms).</span></span> <span data-ttu-id="fda5e-123">このプロセスに必要な具体的な手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fda5e-123">The specific steps that are needed for this process include:</span></span>

    1. <span data-ttu-id="fda5e-124">各 VM で実行する必要があるスクリプトをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="fda5e-124">Export the scripts that must be run on each VM.</span></span>
    
        ```powershell
        # Export the script files to be executed on each VM into a directory VMs\<VMName>
        .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```

    2. <span data-ttu-id="fda5e-125">各インフラストラクチャ\\VM<VMName>フォルダーのコンテンツを、対応する VM にコピーし (リモート処理スクリプトが使用されている場合は、コンテンツをターゲット VM に自動的にコピーします)、存在する場合は次のスクリプトを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-125">Copy the contents of each infrastructure\\VMs<VMName> folder into the corresponding VM (if remoting scripts are used, they will automatically copy the content to the target VMs), and then run the following scripts, if they exist.</span></span> <span data-ttu-id="fda5e-126">これらの手順を管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-126">Perform these steps as an Administrator.</span></span>
    
        ```powershell
        # If remoting, only execute
        # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ForcePushLBDScripts

        .\Import-PfxFiles.ps1
        .\Set-CertificateAcls.ps1
        ```
        
    3. <span data-ttu-id="fda5e-127">次のスクリプトを実行して VM のセットアップを検証します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-127">Run the following script to validate the VM setup.</span></span>
    
        ```powershell
        # If remoting, only execute
        # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        .\Test-D365FOConfiguration.ps1
        ```

6. <span data-ttu-id="fda5e-128">Axdataenciphermentcert 証明書がローテーションされている場合は、資格情報の .json ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-128">If axdataenciphermentcert certificates are rotated, you need to regenerate the credentials.json file.</span></span> <span data-ttu-id="fda5e-129">詳細については、「[資格情報の暗号化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#encryptcred)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-129">For more information, see [Encrypt credentials](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#encryptcred).</span></span>

7. <span data-ttu-id="fda5e-130">後で LCS で使用できる値を保持するには、次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-130">Run the following PowerShell command to have values that can be used in LCS later.</span></span> <span data-ttu-id="fda5e-131">詳細については、[LCS からのオンプレミス環境の配置](setup-deploy-on-premises-pu12.md#deploy) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-131">For more information, see [Deploy your on-premises environment from LCS](setup-deploy-on-premises-pu12.md#deploy).</span></span>

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```


## <a name="activate-new-certificates-within-service-fabric-cluster"></a><span data-ttu-id="fda5e-132">Service Fabric cluster 内での新しい証明書のアクティブ化</span><span class="sxs-lookup"><span data-stu-id="fda5e-132">Activate new certificates within Service Fabric cluster</span></span>

### <a name="service-fabric-with-certificates-that-arent-expired"></a><a name="sfcertrotationnotexpired"></a><span data-ttu-id="fda5e-133">期限切れになっていない証明書を含む Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fda5e-133">Service Fabric with certificates that aren't expired</span></span>

1. <span data-ttu-id="fda5e-134">編集するために **Clusterconfig.json** ファイルを開き、次のセクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-134">Open the **Clusterconfig.json** file for editing, and find the following section.</span></span> <span data-ttu-id="fda5e-135">セカンダリ サムプリントが定義されている場合は、先に進む前に、[古い Service Fabric 証明書をクリーンアップ](#cleanupoldsfcerts) に移動します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-135">If a secondary thumbprint is defined, go to [Clean up old Service Fabric certificates](#cleanupoldsfcerts) before you go any further.</span></span>

    ```json
    "security": {
        "metadata":  "The Credential type X509 indicates this cluster is secured using X509 Certificates. 
        The thumbprint format is - d5 ec 42 3b 79 cb e5 07 fd 83 59 3c 56 b9 d5 31 24 25 42 64.",
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

2. <span data-ttu-id="fda5e-136">ファイルのそのセクションを、次のセクションと置換します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-136">Replace that section in the file with following section.</span></span>

    ```json
    "security":  {
        "metadata":  "The Credential type X509 indicates this cluster is secured using X509 Certificates. 
        The thumbprint format is - d5 ec 42 3b 79 cb e5 07 fd 83 59 3c 56 b9 d5 31 24 25 42 64.",
        "ClusterCredentialType":  "X509",
        "ServerCredentialType":  "X509",
        "CertificateInformation":  {
            "ClusterCertificate":  {
                                       "X509StoreName":  "My",
                                        "Thumbprint": "*New server thumbprint(Star/SF)*",
                                        "ThumbprintSecondary": "Old server thumbprint(Star/SF)"
                                   },
            "ServerCertificate":   {
                                        "X509StoreName":  "My",
                                        "Thumbprint": "*New server thumbprint(Star/SF)*",
                                        "ThumbprintSecondary": "Old server thumbprint(Star/SF)"
                                   },
            "ClientCertificateThumbprints":  [
                                       {
                                            "CertificateThumbprint": "*Old client thumbprint*",
                                            "IsAdmin":  false
                                       },
                                       {
                                            "CertificateThumbprint": "*New client thumbprint*",
                                            "IsAdmin":  true
                                       }
                                             ]
                                   }
                },
    ```

3. <span data-ttu-id="fda5e-137">新しいサムプリントと古いサムプリント値を編集します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-137">Edit the new and old thumbprint values.</span></span> 

4. <span data-ttu-id="fda5e-138">2.0.0 などの clusterConfigurationVersion を新しいバージョンに変更します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-138">Change clusterConfigurationVersion to the new version, for example 2.0.0.</span></span>

    ```json
    {
    "name": "Dynamics365Operations",
    "clusterConfigurationVersion": "2.0.0",
    "apiVersion": "10-2017",
    ```
    
5. <span data-ttu-id="fda5e-139">Clusterconfig.json ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-139">Save the new ClusterConfig.json file.</span></span>

6. <span data-ttu-id="fda5e-140">次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-140">Run the following PowerShell command.</span></span>

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

### <a name="service-fabric-with-or-without-expired-certificates-cluster-not-accessible"></a><span data-ttu-id="fda5e-141">期限が切れた証明書 (クラスターにアクセスできない)を含むまたは含まないサービスファブリック</span><span class="sxs-lookup"><span data-stu-id="fda5e-141">Service Fabric with or without expired certificates (cluster not accessible)</span></span>

<span data-ttu-id="fda5e-142">このプロセスを続行するには、 [オンプレミスの展開のトラブルシューティング](troubleshoot-on-prem.md#clean-up-an-existing-environment-and-redeploy) を行ってください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-142">Continue this process following [Troubleshoot on-premises deployments](troubleshoot-on-prem.md#clean-up-an-existing-environment-and-redeploy).</span></span>

## <a name="update-the-localagent-certificate"></a><span data-ttu-id="fda5e-143">LocalAgent 証明書を更新する</span><span class="sxs-lookup"><span data-stu-id="fda5e-143">Update the LocalAgent certificate</span></span>

<span data-ttu-id="fda5e-144">次の場合は、LocalAgent を再インストールする必要があります:</span><span class="sxs-lookup"><span data-stu-id="fda5e-144">You must reinstall the LocalAgent if:</span></span>

- <span data-ttu-id="fda5e-145">Service Fabric Cluster/サーバー証明書を変更しました。</span><span class="sxs-lookup"><span data-stu-id="fda5e-145">You changed the service fabric cluster/server certificate.</span></span>
- <span data-ttu-id="fda5e-146">Service Fabric クライアント証明書を変更しました。</span><span class="sxs-lookup"><span data-stu-id="fda5e-146">You changed the service fabric client certificate.</span></span>
- <span data-ttu-id="fda5e-147">LocalAgent 証明書を更新しました。</span><span class="sxs-lookup"><span data-stu-id="fda5e-147">You changed the LocalAgent certificate.</span></span>

1. <span data-ttu-id="fda5e-148">いずれかの Orchestrator ノードに対して次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-148">Run the following PowerShell command on one of the Orchestrator nodes.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. <span data-ttu-id="fda5e-149">次の PowerShell コマンドを実行して、新しい LocalAgent の拇印を記録します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-149">Run the following PowerShell command and note the new LocalAgent thumbprint.</span></span>

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

3. <span data-ttu-id="fda5e-150">「[テナント向けの LCS 接続コンフィギュレーション](setup-deploy-on-premises-pu12.md#configurelcs)」の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-150">Follow the steps in [Configure LCS connectivity for the tenant](setup-deploy-on-premises-pu12.md#configurelcs).</span></span>

    > [!NOTE] 
    > <span data-ttu-id="fda5e-151">**KeyId \<key\> による既存の資格情報の更新は許可されていません** というエラー メッセージを受信した場合は、[エラー メッセージ: 「KeyId <key> による既存の資格情報の更新は許可されていません」](troubleshoot-on-prem.md#error-updates-to-existing-credential-with-keyid-key-is-not-allowed) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-151">If you receive the error **Update to existing credential with KeyId '\<key\>' is not allowed**, follow the instructions in [Error: "Updates to existing credential with KeyId '<key>' is not allowed"](troubleshoot-on-prem.md#error-updates-to-existing-credential-with-keyid-key-is-not-allowed).</span></span>

4. <span data-ttu-id="fda5e-152">[コネクタのコンフィギュレーションを続行し、オンプレミスのローカルエージェントをインストールします。](setup-deploy-on-premises-pu12.md#configureconnector)具体的には、次の変更があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-152">Continue with [Configure a connector and install an on-premises local agent](setup-deploy-on-premises-pu12.md#configureconnector), specifically the following changes:</span></span>

    - <span data-ttu-id="fda5e-153">クライアント証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="fda5e-153">Client certificate thumbprint</span></span>
    - <span data-ttu-id="fda5e-154">サーバー証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="fda5e-154">Server certificate thumbprint</span></span>
    - <span data-ttu-id="fda5e-155">テナント サービス プリンシパル証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="fda5e-155">Tenant service principle certificate thumbprint</span></span>

## <a name="update-your-current-deployment-configuration"></a><span data-ttu-id="fda5e-156">現在の配置コンフィギュレーションを更新する</span><span class="sxs-lookup"><span data-stu-id="fda5e-156">Update your current deployment configuration</span></span>

<span data-ttu-id="fda5e-157">証明書を更新すると、環境に存在するコンフィギュレーション ファイルが古くなり、手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-157">Because you've updated your certificates, the configuration file that is present in your environment is outdated and must be manually updated.</span></span> <span data-ttu-id="fda5e-158">そうしないと、クリーンアップ ジョブが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-158">Otherwise, the cleanup job will probably fail.</span></span> <span data-ttu-id="fda5e-159">(この手動更新は、今回だけ行う必要があります。)</span><span class="sxs-lookup"><span data-stu-id="fda5e-159">(This manual update must be done just this one time.)</span></span>

1. <span data-ttu-id="fda5e-160">コンフィギュレーション ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-160">Open your configuration file.</span></span> <span data-ttu-id="fda5e-161">次のコマンドを実行して、このファイルの場所を検索できます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-161">You can find the location of this file by running the following command.</span></span>

    ```sql
    select Location from DeploymentInstanceArtifact where AssetId='config.json' and DeploymentInstanceId = 'LCSENVIRONMENTID'
    ```

    > [!NOTE]
    > <span data-ttu-id="fda5e-162">**LCSENVIRONMENTID** を環境の ID で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-162">Replace **LCSENVIRONMENTID** with the ID of your environment.</span></span> <span data-ttu-id="fda5e-163">このIDは、LCS の環境のページから取得できます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-163">You can obtain this ID from the page for your environment in LCS.</span></span> 

    <span data-ttu-id="fda5e-164">ファイルの先頭は、次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-164">The beginning of the file should resemble the following example.</span></span>

    ```json
    {
    "serviceFabric": {
        "connectionEndpoint": "192.168.8.22:19000",
        "clusterId": "Orch",
        "certificateSettings": {
        "serverCertThumbprint": "Old server thumbprint(Star/SF)",
        "clientCertThumbprint": "Old client thumbprint"
        }
    },
    ```

2. <span data-ttu-id="fda5e-165">**serverCertThumprint** と **clientCertThumbprint** 値を新しいサムプリントで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-165">Replace the **serverCertThumprint** and **clientCertThumbprint** values with the new thumbprints.</span></span>

    ```json
    {
    "serviceFabric": {
        "connectionEndpoint": "192.168.8.22:19000",
        "clusterId": "Orch",
        "certificateSettings": {
        "serverCertThumbprint": "New server thumbprint(Star/SF)",
        "clientCertThumbprint": "New client thumbprint"
        }
    },
    ```

3. <span data-ttu-id="fda5e-166">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-166">Save and close the file.</span></span> <span data-ttu-id="fda5e-167">このネットワークの場所にアクセスするすべてのプログラムを閉じてください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-167">Remember to close any programs that are accessing this network location.</span></span> <span data-ttu-id="fda5e-168">そうしないと、クリーンアップ プロセスが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-168">Otherwise, the cleanup process might fail.</span></span>

## <a name="update-deployment-settings-in-lcs"></a><span data-ttu-id="fda5e-169">LCS の展開設定の更新</span><span class="sxs-lookup"><span data-stu-id="fda5e-169">Update deployment settings in LCS</span></span>

> [!NOTE]
>  <span data-ttu-id="fda5e-170">ただし、クライアント、データ署名、および暗号化証明書は置換のみ行われます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-170">Note that the Client, Data Signing, and Encipherment certificates will only be replaced.</span></span> <span data-ttu-id="fda5e-171">また、「[資格情報の暗号化](setup-deploy-on-premises-pu12.md#encryptcred)」で説明されているように、資格情報の Credentials.json ファイルを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-171">You will also need to recreate the Credentials.json file, as described in [Encrypt credentials](setup-deploy-on-premises-pu12.md#encryptcred).</span></span>
>
> <span data-ttu-id="fda5e-172">続行する前に、ロケール Dynamics データベースのバックアップを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-172">Before you continue, you need to make a backup of the local Dynamics database.</span></span>

1. <span data-ttu-id="fda5e-173">LCS で、証明書の変更を希望する環境についての「完全な詳細情報」リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-173">In LCS, select the "Full Details" link for the environment where you want to change the certificates.</span></span>

2. <span data-ttu-id="fda5e-174">**管理** を選択し、**更新の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-174">Select **Maintain** and then select **Update Settings**.</span></span>

    ![更新設定の適用](media/addf4f1d0c0a86d840a6a412f774e474.png)

3. <span data-ttu-id="fda5e-176">以前にコンフィギュレーションした新しいサムプリントにサムプリントを変更します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-176">Change the thumbprints to the new thumbprints that you previously configured.</span></span> <span data-ttu-id="fda5e-177">これらは、InfrastructureScripts フォルダの ConfigTemplate.xml ファイルで検索できます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-177">You can find them in the ConfigTemplate.xml file in the InfrastructureScripts folder.</span></span>

    ![配置設定のサムプリント画像 1](media/07da4d7e02f11878ee91c61b4f561a50.png)

    ![配置設定のサムプリント画像 2](media/785caaf4ee652d66c0d88cf615a57e26.png)

4. <span data-ttu-id="fda5e-180">**準備** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-180">Select **Prepare**.</span></span>

5. <span data-ttu-id="fda5e-181">ダウンロードおよび準備が完了すると、**環境の更新** ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-181">After downloading and preparation is complete, the **Update environment** button will display.</span></span>

    ![環境の更新ボタン](media/0a9d43044593450f1a828c0dd7698024.png)

6. <span data-ttu-id="fda5e-183">**環境の更新** を選択して、環境の更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-183">Select **Update environment** to start updating your environment.</span></span>

7. <span data-ttu-id="fda5e-184">更新中、環境は使用できません。</span><span class="sxs-lookup"><span data-stu-id="fda5e-184">During the update, the environment will be unavailable.</span></span>

8. <span data-ttu-id="fda5e-185">新しい証明書を使用して環境を正常に更新した後、Service Fabric Cluster エクスプローラーで新しいサムプリントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-185">After the environment is successfully updated with the new certificates, you can view the new thumbprints in Service Fabric Cluster Explorer.</span></span> <span data-ttu-id="fda5e-186">Service Fabric エクスプローラーのサムプリントの名前は、LCS の名前と異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-186">The names of the thumbprints in Service Fabric Explorer might differ from the names in LCS.</span></span> <span data-ttu-id="fda5e-187">ただし、値は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-187">However, the values should be the same.</span></span>

    <span data-ttu-id="fda5e-188">次の例では、同じ拇印の名前がいくらか異なっている例の一部です。</span><span class="sxs-lookup"><span data-stu-id="fda5e-188">Here is an example of how the name of the same thumbprint might differ.</span></span>

    ![配置設定におけるサムプリントの例 1](media/038173714b2fb6cf12acc4bda2a3dde5.png)

    ![配置設定におけるサムプリントの例 2](media/642f6434da9cdeac3651b765acca08fa.png)

## <a name="update-other-certificates-as-needed"></a><span data-ttu-id="fda5e-191">必要に応じて他の証明書を更新する</span><span class="sxs-lookup"><span data-stu-id="fda5e-191">Update other certificates as needed</span></span>

1. <span data-ttu-id="fda5e-192">SQL server 証明書の有効期限が切れていないかどうかを常に確認してください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-192">Always check if the SQL server certificate has expired.</span></span> <span data-ttu-id="fda5e-193">詳細については、「[SQL Server の設定](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#setupsql)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-193">For more information, see [Set up SQL Server](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#setupsql).</span></span>

2. <span data-ttu-id="fda5e-194">Active Directory フェデレーション サービス (ADFS) 証明書の有効期限が切れていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-194">Check to be sure that the Active Directory Federation Service (ADFS) certificate has not expired.</span></span>

## <a name="clean-up-old-service-fabric-certificates"></a><a name="cleanupoldsfcerts"></a><span data-ttu-id="fda5e-195">古い Service Fabric 証明書をクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="fda5e-195">Clean up old Service Fabric certificates</span></span>

<span data-ttu-id="fda5e-196">この手順は、証明書のローテーションが成功した後、または次の証明書のローテーションの前に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-196">This procedure should be completed either after a successful certificate rotation or before the next certificate rotation.</span></span>

1. <span data-ttu-id="fda5e-197">クラスター構成から古い/セカンダリのサムプリントを削除します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-197">Remove the old/secondary thumbprints from the cluster configuration.</span></span> <span data-ttu-id="fda5e-198">これらを削除した後、適切なセクションは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-198">After you've removed them, the appropriate section should resemble the following example.</span></span>

    ```json
    "security": {
        "metadata":  "The Credential type X509 indicates this is cluster is secured using X509 Certificates.
        The thumbprint format is - d5 ec 42 3b 79 cb e5 07 fd 83 59 3c 56 b9 d5 31 24 25 42 64.",
        "ClusterCredentialType":  "X509",
        "ServerCredentialType":  "X509",
        "CertificateInformation":  {
            "ClusterCertificate":  {
                                       "X509StoreName":  "My",
                                        "Thumbprint": "server thumbprint(Star/SF)"
                                   },
            "ServerCertificate":   {
                                        "X509StoreName":  "My",
                                        "Thumbprint": "server thumbprint(Star/SF)"
                                   },
            "ClientCertificateThumbprints":  [
                                       {
                                            "CertificateThumbprint": "client thumbprint",
                                            "IsAdmin":  true
                                       }
                                             ]
                                   }
                },
    ```

1. <span data-ttu-id="fda5e-199">このトピックの前半の [期限切れになっていない証明書を含む Service Fabric](#sfcertrotationnotexpired) セクションの手順 4 から 6 を実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-199">Follow steps 4 through 6 in the [Service Fabric with certificates that are not expired](#sfcertrotationnotexpired) section earlier in this topic.</span></span> 

## <a name="after-certificate-rotation"></a><a name="aftercertrotation"></a><span data-ttu-id="fda5e-200">証明書ローテーション後</span><span class="sxs-lookup"><span data-stu-id="fda5e-200">After certificate rotation</span></span>

### <a name="data-encryption-certificate"></a><span data-ttu-id="fda5e-201">データの暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="fda5e-201">Data encryption certificate</span></span>

<span data-ttu-id="fda5e-202">この証明書は、データベースに格納されているデータを暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-202">This certificate is used to encrypt data stored in the database.</span></span> <span data-ttu-id="fda5e-203">既定では、この証明書を使用して暗号化される特定のフィールドがあります。これらのフィールドは、[暗号化されたフィールドの値を文書化](../database/dbmovement-scenario-goldenconfig.md#document-the-values-of-encrypted-fields) で確認できます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-203">By default there are certain fields that are encrypted with this certificate, you can check those fields in [Document the values of encrypted fields](../database/dbmovement-scenario-goldenconfig.md#document-the-values-of-encrypted-fields).</span></span> <span data-ttu-id="fda5e-204">ただし、この API を使用して、ユーザーが暗号化すべきと判断した他のフィールドを暗号化することができます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-204">However, our API can be used to encrypt other fields that customers deem should be encrypted.</span></span> 

<span data-ttu-id="fda5e-205">プラットフォーム更新 33 以降では、「暗号化されたデータ ローテーション システム ジョブ」という名前のバッチ ジョブが、新しくローテーションした証明書を使用してデータを再暗号化します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-205">In Platform update 33 and later, the batch job that is named "Encrypted data rotation system job" will use the newly rotated certificate to re-encrypt data.</span></span> <span data-ttu-id="fda5e-206">このバッチ ジョブは、データをクロールし、新しい証明書を使用してすべての暗号化データを再暗号化します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-206">This batch job crawls through your data to re-encrypt all the encrypted data by using the new certificate.</span></span> <span data-ttu-id="fda5e-207">これは、すべてのデータが再度暗号化されるまで、1 日に 2 時間実行されます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-207">It will run for two hours per day until all of the data has been re-encrypted.</span></span> <span data-ttu-id="fda5e-208">バッチ ジョブを有効にするには、フライトとコンフィギュレーション キーを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-208">In order to enable the batch job, a flight and a configuration key need to be enabled.</span></span> <span data-ttu-id="fda5e-209">業務データベース (AXDB など) に対して次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-209">Execute the following commands against your business database (for example, AXDB).</span></span>

```sql
IF (EXISTS(SELECT * FROM SYSFLIGHTING WHERE [FLIGHTNAME] = 'EnableEncryptedDataCrawlerRotationTask'))
  UPDATE SYSFLIGHTING SET [ENABLED] = 1 WHERE [FLIGHTNAME] = 'EnableEncryptedDataCrawlerRotationTask'
ELSE
  INSERT INTO SYSFLIGHTING ([FLIGHTNAME],[ENABLED],[FLIGHTSERVICEID]) VALUES ('EnableEncryptedDataCrawlerRotationTask', 1, 0)
 
IF (EXISTS(SELECT * FROM SECURITYCONFIG WHERE [KEY_] = 'EnableEncryptedDataRotation'))
  UPDATE SECURITYCONFIG SET [VALUE] = 'True' WHERE [KEY_] = 'EnableEncryptedDataRotation'
ELSE
  INSERT INTO SECURITYCONFIG ([KEY_], [VALUE]) VALUES ('EnableEncryptedDataRotation', 'True')
```

<span data-ttu-id="fda5e-210">上記のコマンドを実行した後、Service Fabric Explorer から AOS ノードを再起動します。</span><span class="sxs-lookup"><span data-stu-id="fda5e-210">After the above commands have been executed, restart your AOS nodes from Service Fabric Explorer.</span></span> <span data-ttu-id="fda5e-211">AOS によって新しいコンフィギュレーションが検出され、業務時間外にバッチ ジョブが実行されるようにスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-211">The AOS will detect the new configuration and will schedule the batch job to run during off hours.</span></span> <span data-ttu-id="fda5e-212">バッチ ジョブを作成した後、ユーザー インターフェイスからスケジュールを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fda5e-212">After the batch job has been created, the schedule can be modified from the user interface.</span></span>

> [!WARNING]
> <span data-ttu-id="fda5e-213">暗号化されたデータがすべて再暗号化され、期限が切れるまでは、古いデータ暗号化証明書が削除されなうようにしてください。</span><span class="sxs-lookup"><span data-stu-id="fda5e-213">Make sure that the old Data Encryption certificate is not removed before all encrypted data has been re-encrypted and it has not expired.</span></span> <span data-ttu-id="fda5e-214">そうしないと、これによってデータが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fda5e-214">Otherwise, this could lead to data loss.</span></span>
