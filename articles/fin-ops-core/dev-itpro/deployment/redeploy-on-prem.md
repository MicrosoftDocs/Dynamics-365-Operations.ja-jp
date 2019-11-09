---
title: オンプレミス環境の再配置
description: このトピックでは、オンプレミス環境の再展開について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 3df2d7556599a14b3e7b481122e6424b0c932771
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183383"
---
# <a name="redeploy-on-premises-environments"></a><span data-ttu-id="c2245-103">オンプレミス環境の再配置</span><span class="sxs-lookup"><span data-stu-id="c2245-103">Redeploy on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2245-104">ある時点で、オンプレミス環境を再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2245-104">At some point, you might have to redeploy your on-premises environment.</span></span> <span data-ttu-id="c2245-105">これは、新しいプラットフォームの更新または実装の変更や問題がある場合に適用できます。</span><span class="sxs-lookup"><span data-stu-id="c2245-105">This could be to apply a new platform update or because of changes or issues in your implementation.</span></span> <span data-ttu-id="c2245-106">現在使用している環境を削除する前に、再配置する際に使用するコンフィギュレーション設定情報を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2245-106">Before you delete the environment you are currently working with, you should save your configuration setting information to use when you redeploy.</span></span> <span data-ttu-id="c2245-107">このトピックでは、構成設定を保存する方法と、環境を再配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c2245-107">This topic describes how to save configuration settings and how to redeploy your environment.</span></span> 

## <a name="save-your-configuration"></a><span data-ttu-id="c2245-108">コンフィギュレーションの保存</span><span class="sxs-lookup"><span data-stu-id="c2245-108">Save your configuration</span></span>
<span data-ttu-id="c2245-109">更新する予定の環境を削除する前に、次の手順に従って構成を保存してください。</span><span class="sxs-lookup"><span data-stu-id="c2245-109">Before you delete the environment you plan to update, use the following steps to save your configuration.</span></span> 
1. <span data-ttu-id="c2245-110">LCS で、**プロジェクト設定** > **オンプレミス コネクタ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2245-110">In LCS, navigate to **Project Settings** > **On-prem Connectors**.</span></span>
2. <span data-ttu-id="c2245-111">環境へのコネクタを選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2245-111">Select the connector to your environment, and then click **Edit**.</span></span>
3. <span data-ttu-id="c2245-112">**コネクタの編集**タブで、**エージェントの構成** > **コンフィギュレーションの入力**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2245-112">On the **Edit connector** tab, navigate to **Configure Agent** > **Enter Configuration**.</span></span>
4. <span data-ttu-id="c2245-113">**コンフィギュレーション設定**セクションのダウンロード Fileshare 場所の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="c2245-113">Copy the value of the Download Fileshare location in the **Configuration Settings** section.</span></span> <span data-ttu-id="c2245-114">これは後で必要になります。</span><span class="sxs-lookup"><span data-stu-id="c2245-114">You will need this later.</span></span>
5. <span data-ttu-id="c2245-115">オンプレミス環境ファイル共有マシンにログインして、**\agent\wp<environment name>\StandaloneSetup\config.json** をコピーします。</span><span class="sxs-lookup"><span data-stu-id="c2245-115">Log in to the on-premises environment file share machine and copy the **\agent\wp<environment name>\StandaloneSetup\config.json**.</span></span> <span data-ttu-id="c2245-116">この json ファイルで構成設定を使用すると、環境を再配置することができます。</span><span class="sxs-lookup"><span data-stu-id="c2245-116">You can use the configuration settings in this json file to redeploy your environment.</span></span>

### <a name="configuration-settings"></a><span data-ttu-id="c2245-117">コンフィギュレーション設定</span><span class="sxs-lookup"><span data-stu-id="c2245-117">Configuration settings</span></span>
<span data-ttu-id="c2245-118">次のテーブルに、コンフィギュレーション設定に関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="c2245-118">The following tables provide information about configuration settings.</span></span> <span data-ttu-id="c2245-119">前の手順で保存した .json ファイルの**構成設定**値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c2245-119">Use the **Configuration setting** value from the .json file that you saved in the previous procedure.</span></span>

<span data-ttu-id="c2245-120">**Active Directory フェデレーション サービス設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-120">**Active Directory Federation Services settings**</span></span>


|                                                                  <span data-ttu-id="c2245-121"><strong>フィールド</strong></span><span class="sxs-lookup"><span data-stu-id="c2245-121"><strong>Field</strong></span></span>                                                                  |                          <span data-ttu-id="c2245-122"><strong>コンフィギュレーション設定</strong></span><span class="sxs-lookup"><span data-stu-id="c2245-122"><strong>Configuration setting</strong></span></span>                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
|                         <span data-ttu-id="c2245-123">最初の管理者になるユーザーの電子メール アドレス (たとえば、adminuser@yourdomain.com)</span><span class="sxs-lookup"><span data-stu-id="c2245-123">The email address of the user who will be the initial administrator (such as, adminuser@yourdomain.com)</span></span>                          |            <span data-ttu-id="c2245-124">components.(AOS).parameters.provisioning.adminPrincipleName.value</span><span class="sxs-lookup"><span data-stu-id="c2245-124">components.(AOS).parameters.provisioning.adminPrincipleName.value</span></span>             |
| <span data-ttu-id="c2245-125">Dynamics 365 アプリケーション グループの ADFS OpenID メタデータ エンドポイント。</span><span class="sxs-lookup"><span data-stu-id="c2245-125">ADFS OpenID metadata endpoint for the Dynamics 365 Application group.</span></span> <span data-ttu-id="c2245-126">(https://[federation-service-name]/adfs/.well-known/openid-configuration など)</span><span class="sxs-lookup"><span data-stu-id="c2245-126">(such as, https://[federation-service-name]/adfs/.well-known/openid-configuration)</span></span> |              <span data-ttu-id="c2245-127">components.(AOS).parameters.activeDirectory.adfsMetadata.value</span><span class="sxs-lookup"><span data-stu-id="c2245-127">components.(AOS).parameters.activeDirectory.adfsMetadata.value</span></span>              |
|                                               <span data-ttu-id="c2245-128">AOS アプリケーション グループの ADFS OpenID 接続クライアント ID</span><span class="sxs-lookup"><span data-stu-id="c2245-128">ADFS OpenID Connect client ID for the AOS application group</span></span>                                                |              <span data-ttu-id="c2245-129">components.(AOS).parameters.activeDirectory.adfsClientId.value</span><span class="sxs-lookup"><span data-stu-id="c2245-129">components.(AOS).parameters.activeDirectory.adfsClientId.value</span></span>              |
|                                       <span data-ttu-id="c2245-130">Financial Reporting アプリケーション グループの ADFS OpenID 接続クライアント ID</span><span class="sxs-lookup"><span data-stu-id="c2245-130">ADFS OpenID Connect client ID for the Financial Reporting application group</span></span>                                        | <span data-ttu-id="c2245-131">components.(FinancialReporting).parameters.aad.nativeClientAuthentication.clientId.value</span><span class="sxs-lookup"><span data-stu-id="c2245-131">components.(FinancialReporting).parameters.aad.nativeClientAuthentication.clientId.value</span></span> |

<span data-ttu-id="c2245-132">**SQL データベース コンフィギュレーション**</span><span class="sxs-lookup"><span data-stu-id="c2245-132">**SQL database configuration**</span></span>

| <span data-ttu-id="c2245-133">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="c2245-133">**Field**</span></span>                        | <span data-ttu-id="c2245-134">**コンフィギュレーション設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-134">**Configuration setting**</span></span>                                                              |
|------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2245-135">SQL Server</span><span class="sxs-lookup"><span data-stu-id="c2245-135">SQL SERVER</span></span>                   | <span data-ttu-id="c2245-136">components.(AOS).parameters.database.dbServer.value</span><span class="sxs-lookup"><span data-stu-id="c2245-136">components.(AOS).parameters.database.dbServer.value</span></span>          |
| <span data-ttu-id="c2245-137">AX データベース</span><span class="sxs-lookup"><span data-stu-id="c2245-137">AX DATABASE</span></span>                  | <span data-ttu-id="c2245-138">components.(AOS).parameters.database.dbName.value</span><span class="sxs-lookup"><span data-stu-id="c2245-138">components.(AOS).parameters.database.dbName.value</span></span>            |
| <span data-ttu-id="c2245-139">FINANCIAL REPORTING DATABASE</span><span class="sxs-lookup"><span data-stu-id="c2245-139">FINANCIAL REPORTING DATABASE</span></span> | <span data-ttu-id="c2245-140">components.(FinancialReporting).parameters.mrdb.dbName.value</span><span class="sxs-lookup"><span data-stu-id="c2245-140">components.(FinancialReporting).parameters.mrdb.dbName.value</span></span> |

<span data-ttu-id="c2245-141">**ファイル共有設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-141">**File share settings**</span></span>

| <span data-ttu-id="c2245-142">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="c2245-142">**Field**</span></span>                                                                                                                              | <span data-ttu-id="c2245-143">**コンフィギュレーション設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-143">**Configuration setting**</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2245-144">Microsoft Dynamics 365 インスタンスのファイル共有パス。</span><span class="sxs-lookup"><span data-stu-id="c2245-144">The file share path for the Microsoft Dynamics 365 instance.</span></span> <span data-ttu-id="c2245-145">この共有は、ユーザーがアップロードしたファイルのドキュメント ストアとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="c2245-145">This share is used as the document store for files uploaded by users.</span></span> | <span data-ttu-id="c2245-146">components.(AOS).parameters.storage.fileSharePath.value</span><span class="sxs-lookup"><span data-stu-id="c2245-146">components.(AOS).parameters.storage.fileSharePath.value</span></span>          |
| <span data-ttu-id="c2245-147">Microsoft Dynamics 365 インスタンスのファイル共有証明書の拇印。</span><span class="sxs-lookup"><span data-stu-id="c2245-147">The File share certificate thumbprint for the Microsoft Dynamics 365 instance.</span></span>                                                      | <span data-ttu-id="c2245-148">components.(AOS).parameters.storage.sharedAccessThumbprint.value</span><span class="sxs-lookup"><span data-stu-id="c2245-148">components.(AOS).parameters.storage.sharedAccessThumbprint.value</span></span> |

   > [!NOTE]
   > <span data-ttu-id="c2245-149">ファイル パス コンフィギュレーション値を .json ファイルから LCS UI にコピーするときは、余分な円記号をかならず削除してください。</span><span class="sxs-lookup"><span data-stu-id="c2245-149">When you copy the file path configuration value from .json file to LCS UI, make sure to remove the extra backslashes.</span></span> <span data-ttu-id="c2245-150">たとえば、.json ファイルからのコンフィギュレーション値 **\\\\DC1\\D365FFOStorage** は LCS UI で **\\DC1\D365FFOStorage** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2245-150">For example, configuration value **\\\\DC1\\D365FFOStorage** from the .json file should be **\\DC1\D365FFOStorage** in the LCS UI.</span></span>

<span data-ttu-id="c2245-151">**SSRS コンフィギュレーション設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-151">**SSRS configuration settings**</span></span>

| <span data-ttu-id="c2245-152">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="c2245-152">**Field**</span></span>                                                                      | <span data-ttu-id="c2245-153">**コンフィギュレーション設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-153">**Configuration setting**</span></span>                                                                                      |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2245-154">SSRS インスタンスの IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="c2245-154">The IP Address of the SSRS instance.</span></span>                                        | <span data-ttu-id="c2245-155">components.(AOS).parameters.biReporting.persistentVirtualMachineIPAddressSSRS.value</span><span class="sxs-lookup"><span data-stu-id="c2245-155">components.(AOS).parameters.biReporting.persistentVirtualMachineIPAddressSSRS.value</span></span>  |
| <span data-ttu-id="c2245-156">SSRS アプリケーションが AX サービスと通信するために使用するサムプリント。</span><span class="sxs-lookup"><span data-stu-id="c2245-156">The thumbprint used by the SSRS application to communicate with AX Service.</span></span> | <span data-ttu-id="c2245-157">components.(ReportingServices).parameters.reportingClientCertificateThumbprint.value</span><span class="sxs-lookup"><span data-stu-id="c2245-157">components.(ReportingServices).parameters.reportingClientCertificateThumbprint.value</span></span> |

<span data-ttu-id="c2245-158">**サービスの設定のコンフィギュレーション**</span><span class="sxs-lookup"><span data-stu-id="c2245-158">**Configure service settings**</span></span>

| <span data-ttu-id="c2245-159">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="c2245-159">**Field**</span></span>                                                                                                                                      | <span data-ttu-id="c2245-160">**コンフィギュレーション設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-160">**Configuration setting**</span></span>                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2245-161">Dynamics 365 DNS 情報 - Microsoft Dynamics 365 インスタンスの DNS ホスト名 (ax.d365ffo.onprem.contoso.com など)。</span><span class="sxs-lookup"><span data-stu-id="c2245-161">DYNAMICS 365 DNS INFORMATION - The DNS host name of the Microsoft Dynamics 365 instance, such as ax.d365ffo.onprem.contoso.com.</span></span>           | <span data-ttu-id="c2245-162">components.(AOS).parameters.infrastructure.hostName</span><span class="sxs-lookup"><span data-stu-id="c2245-162">components.(AOS).parameters.infrastructure.hostName</span></span>                                            |
| <span data-ttu-id="c2245-163">AOS SERVICE PRINCIPAL USER SETTINGS - yourdomain\axserviceuser など、AX サービスを実行するドメイン ユーザー アカウント。</span><span class="sxs-lookup"><span data-stu-id="c2245-163">AOS SERVICE PRINCIPAL USER SETTINGS - The domain user account to run the AX service, such as yourdomain\axserviceuser.</span></span>                         | <span data-ttu-id="c2245-164">components.(AOS).parameters.infrastructure.principalUserAccountName \*</span><span class="sxs-lookup"><span data-stu-id="c2245-164">components.(AOS).parameters.infrastructure.principalUserAccountName \*</span></span>                          |
| <span data-ttu-id="c2245-165">MR サービス プリンシパル ユーザー設定 - yourdomain\Svc-FRAS$ などの MR アプリケーション サービスを実行するためのグループ管理サービス アカウント (gMSA) です。</span><span class="sxs-lookup"><span data-stu-id="c2245-165">MR SERVICE PRINCIPAL USER SETTINGS - The group managed service account (gMSA) to run the MR application service, such as yourdomain\Svc-FRAS$.</span></span> | <span data-ttu-id="c2245-166">components.(FinancialReporting).parameters.ApplicationServicePrincipalUser.accountName.value \*</span><span class="sxs-lookup"><span data-stu-id="c2245-166">components.(FinancialReporting).parameters.ApplicationServicePrincipalUser.accountName.value \*</span></span> |
| <span data-ttu-id="c2245-167">yourdomain\Svc-FRPS$ などの MR プロセス サービスを実行するためのグループ管理サービス アカウント (gMSA) です。</span><span class="sxs-lookup"><span data-stu-id="c2245-167">The group managed service account (gMSA) to run the MR process service, such as yourdomain\Svc-FRPS$.</span></span>                                          | <span data-ttu-id="c2245-168">components.(FinancialReporting).parameters.ProcessServicePrincipalUser.accountName.value \*</span><span class="sxs-lookup"><span data-stu-id="c2245-168">components.(FinancialReporting).parameters.ProcessServicePrincipalUser.accountName.value \*</span></span>     |
| <span data-ttu-id="c2245-169">yourdomain\Svc-FRCO$ などのクリックワンス サービスを実行するためのグループ管理サービス アカウント (gMSA) です。</span><span class="sxs-lookup"><span data-stu-id="c2245-169">The group managed service account (gMSA) to run the MR click-once service, such as yourdomain\Svc-FRCO$.</span></span>                                       | <span data-ttu-id="c2245-170">components.(FinancialReporting).parameters.ClickOnceServicePrincipalUser.accountName.value \*</span><span class="sxs-lookup"><span data-stu-id="c2245-170">components.(FinancialReporting).parameters.ClickOnceServicePrincipalUser.accountName.value \*</span></span>   |

> [!NOTE]
> <span data-ttu-id="c2245-171">LCS ユーザー インターフェイスで入力する前に、.json ファイルのプリンシパル ユーザー名構成値から余分な円記号を削除します。</span><span class="sxs-lookup"><span data-stu-id="c2245-171">Remove the extra backslash from the Principal username cofiguration value in the .json file before entering in the LCS UI.</span></span> <span data-ttu-id="c2245-172">たとえば、contoso\\AXServiceUser は LCS で contoso\AXServiceUser として入力される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2245-172">For example, contoso\\AXServiceUser should be entered as contoso\AXServiceUser in LCS.</span></span>

<span data-ttu-id="c2245-173">**アプリケーション証明書の設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-173">**Application certificate settings**</span></span>

| <span data-ttu-id="c2245-174">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="c2245-174">**Field**</span></span>                                                                         | <span data-ttu-id="c2245-175">**コンフィギュレーション設定**</span><span class="sxs-lookup"><span data-stu-id="c2245-175">**Configuration setting**</span></span>                                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2245-176">データ暗号化証明書のサムプリント。</span><span class="sxs-lookup"><span data-stu-id="c2245-176">The thumbprint of the Data Encryption certificate.</span></span>                             | <span data-ttu-id="c2245-177">components.(AOS).parameters.database.dataEncryptionCertificateThumbprint.value</span><span class="sxs-lookup"><span data-stu-id="c2245-177">components.(AOS).parameters.database.dataEncryptionCertificateThumbprint.value</span></span>              |
| <span data-ttu-id="c2245-178">データ署名証明書のサムプリント。</span><span class="sxs-lookup"><span data-stu-id="c2245-178">The thumbprint of the Data Signing certificate.</span></span>                                | <span data-ttu-id="c2245-179">components.(AOS).parameters.database.dataSigningCertificateThumbprint.value</span><span class="sxs-lookup"><span data-stu-id="c2245-179">components.(AOS).parameters.database.dataSigningCertificateThumbprint.value</span></span>                 |
| <span data-ttu-id="c2245-180">セッション認証証明書のサムプリント。</span><span class="sxs-lookup"><span data-stu-id="c2245-180">The thumbprint of the Session Authentication certificate.</span></span>                      | <span data-ttu-id="c2245-181">components.(FinancialReporting).parameters.sessionAuthenticationCertificateThumbprint.value</span><span class="sxs-lookup"><span data-stu-id="c2245-181">components.(FinancialReporting).parameters.sessionAuthenticationCertificateThumbprint.value</span></span> |
| <span data-ttu-id="c2245-182">WCF / SOAP サポートに使用される SSL 証明書のサムプリント。</span><span class="sxs-lookup"><span data-stu-id="c2245-182">The thumbprint of the SSL vertificate used for WCF/SOAP support.</span></span>               | <span data-ttu-id="c2245-183">components.(AOS).parameters.infrastructure.sslCertificateThumbprint.value</span><span class="sxs-lookup"><span data-stu-id="c2245-183">components.(AOS).parameters.infrastructure.sslCertificateThumbprint.value</span></span>                   |
| <span data-ttu-id="c2245-184">Management Reporter が AX サービスと通信するために使用するサムプリント。</span><span class="sxs-lookup"><span data-stu-id="c2245-184">The thumbprint used by the Management Reporter to communicate with AX service.</span></span> | <span data-ttu-id="c2245-185">components.(FinancialReporting).parameters.tokenSpec.certThumbprint.value</span><span class="sxs-lookup"><span data-stu-id="c2245-185">components.(FinancialReporting).parameters.tokenSpec.certThumbprint.value</span></span>                   |



## <a name="redeploy-your-environment"></a><span data-ttu-id="c2245-186">環境の再配置</span><span class="sxs-lookup"><span data-stu-id="c2245-186">Redeploy your environment</span></span>
<span data-ttu-id="c2245-187">次の手順では、環境を新しいプラットフォームまたはトポロジで更新または再配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c2245-187">The following instructions provide information about how to update or redeploy your environment with a new platform or topology.</span></span>
1. <span data-ttu-id="c2245-188">LCS で、オンプレミスのプロジェクトの**環境**ブレードに移動します。</span><span class="sxs-lookup"><span data-stu-id="c2245-188">In LCS, navigate to the **Environments** blade in your on-premises project.</span></span>
2. <span data-ttu-id="c2245-189">環境を削除するには、**削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2245-189">Click **Delete** to delete your environment.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="c2245-190">環境を削除しても、データベース、インフラストラクチャ、またはローカル エージェントは削除されません。</span><span class="sxs-lookup"><span data-stu-id="c2245-190">Deleting the environment will not delete the database, infrastructure or Local agent.</span></span> <span data-ttu-id="c2245-191">Service Fabric アプリケーションのみ削除されます。</span><span class="sxs-lookup"><span data-stu-id="c2245-191">Only the Service Fabric applications are deleted.</span></span>

3. <span data-ttu-id="c2245-192">しばらく待ってから、配置が削除されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c2245-192">Wait for a few minutes and verify that the deployment is deleted.</span></span> <span data-ttu-id="c2245-193">展開が削除されたことを確認するには、オンプレミス環境にログインし、[Service Fabric Explorer] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2245-193">To confirm the deployment is deleted, log in to the on-premises environment and navigate to the Service Fabric Explorer.</span></span>

    <span data-ttu-id="c2245-194">次のアプリケーションを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2245-194">The following applications should be deleted:</span></span>
   - <span data-ttu-id="c2245-195">AXBootstapperAppType</span><span class="sxs-lookup"><span data-stu-id="c2245-195">AXBootstapperAppType</span></span>
   - <span data-ttu-id="c2245-196">AXSFType</span><span class="sxs-lookup"><span data-stu-id="c2245-196">AXSFType</span></span>
   - <span data-ttu-id="c2245-197">FinancialReportingType</span><span class="sxs-lookup"><span data-stu-id="c2245-197">FinancialReportingType</span></span>
   - <span data-ttu-id="c2245-198">RTGatewayAppType</span><span class="sxs-lookup"><span data-stu-id="c2245-198">RTGatewayAppType</span></span>
   - <span data-ttu-id="c2245-199">ReportingService</span><span class="sxs-lookup"><span data-stu-id="c2245-199">ReportingService</span></span>

     <span data-ttu-id="c2245-200">次のオンプレミス サービス ファブリック エージェント アプリケーションは削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="c2245-200">The following on-premises service fabric agent applications should not be deleted:</span></span>
   - <span data-ttu-id="c2245-201">LocalAgentType</span><span class="sxs-lookup"><span data-stu-id="c2245-201">LocalAgentType</span></span>
   - <span data-ttu-id="c2245-202">MonitoringAgentAppType</span><span class="sxs-lookup"><span data-stu-id="c2245-202">MonitoringAgentAppType</span></span>

4. <span data-ttu-id="c2245-203">手順 3 でアプリケーションがすべて削除された後、LCS に戻り、**コンフィギュレーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2245-203">After all of the applications in step 3 are deleted, go back to LCS and click **Configure**.</span></span>
5. <span data-ttu-id="c2245-204">プラットフォームの新しいトポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2245-204">Select the new topology for your platform.</span></span>
6. <span data-ttu-id="c2245-205">環境名を入力します。</span><span class="sxs-lookup"><span data-stu-id="c2245-205">Enter the environment name.</span></span> <span data-ttu-id="c2245-206">同じ名前を使用したり、新しい名前を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="c2245-206">You can use the same name or enter a new one.</span></span>
7. <span data-ttu-id="c2245-207">**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2245-207">Click **Advanced Settings**.</span></span>
   <span data-ttu-id="c2245-208">環境を構成するために保存した .json ファイルから、関連する構成を使用することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c2245-208">You can now use the relevant configurations from the .json file that you saved to configure your environment.</span></span>


