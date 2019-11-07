---
title: コード署名証明書を使用して MPOS に署名する
description: このトピックでは、コード署名証明書を使用して MPOS に署名する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ec6b510e28053c74f2f56b29fd79f1c1764da6e7
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653193"
---
# <a name="sign-mpos-with-a-code-signing-certificate"></a><span data-ttu-id="5a8b9-103">コード署名証明書を使用して MPOS に署名する</span><span class="sxs-lookup"><span data-stu-id="5a8b9-103">Sign MPOS with a code signing certificate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a8b9-104">Modern POS (MPOS) をインストールするには、信頼されたプロバイダーからの署名証明書を使用して MPOS アプリに署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-104">To install Modern POS (MPOS) you must sign the MPOS app with a signing certificate from a trusted provider.</span></span> <span data-ttu-id="5a8b9-105">証明書を使用して MPOS アプリに署名するために、**Retail SDK\\ビルド ツール\\Customization.settings** ファイルにあるオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-105">To sign the MPOS app with a certificate, use one of these options in the **Retail SDK\\Build tool\\Customization.settings** file:</span></span>

- <span data-ttu-id="5a8b9-106">Azure DevOps ビルド ステップのセキュア ファイル タスク部分を追加して、証明書をアップロードしてファイル タスクを保護します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-106">Add the Secure file task part of Azure DevOps build steps and upload the certificate to secure the file task.</span></span> <span data-ttu-id="5a8b9-107">セキュア ファイル タスクの出力パス変数を Customization.settings ファイルのパラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-107">Use the secure file task output path variable as a parameter in the Customization.settings file.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="5a8b9-108">セキュリティで保護されたファイル タスクは、パスワードで保護された証明書をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-108">The Secure File task doesn’t support a password protected certificate.</span></span> <span data-ttu-id="5a8b9-109">このタスクをアップロードする前にパスワードを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-109">You must remove the password before uploading this task.</span></span> <span data-ttu-id="5a8b9-110">証明書は、Azure のセキュリティで保護されたファイル システム タスクにアップロードされるため、このステップのパスワードのみを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-110">Because the certificate is uploaded to the secure file system task in Azure, you can remove the password only for this step.</span></span> <span data-ttu-id="5a8b9-111">ただし、パスワードの削除についてはセキュリティの専門家と話し合って、これがプロジェクトにとって正しいアクションであるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-111">However, you should discuss removing the password with your security experts to determine if this is the correct action for your project.</span></span> <span data-ttu-id="5a8b9-112">ビルド タスクにアップロードされた証明書は、ビルド フロー中にビルド パイプラインによってのみアクセスできます。他のプロセスがアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-112">The certificate uploaded to the build task can be accessed only by the build pipeline during build flow and no other process can access it.</span></span> <span data-ttu-id="5a8b9-113">セキュリティで保護されたファイル タスクを使用する場合、パスワード セキュリティの追加レイヤーは必要ありませんが、これはビルド署名プロセス中に限ります。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-113">Using the Secure File task, the additional layer of password security is not required, however this is only during the build signing process.</span></span> <span data-ttu-id="5a8b9-114">他のシナリオの証明書のパスワードは削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-114">Don’t remove the certificate password for other scenarios.</span></span>
- <span data-ttu-id="5a8b9-115">ファイル システムにある証明書を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-115">Use a certificate that is in the file system.</span></span> <span data-ttu-id="5a8b9-116">これを行うには、証明書をダウンロードまたは生成し、ビルドが実行されているファイル システムに配置します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-116">To do this, download or generate a certificate and place it in the file system where the build is running.</span></span> <span data-ttu-id="5a8b9-117">Visual Studio Online エージェントまたはビルド ユーザーは、このパスとファイルにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-117">The Visual Studio Online agent or build user should have access to this path and file.</span></span>
- <span data-ttu-id="5a8b9-118">拇印を使用してストア内の証明書を検索し、その証明書でサインインします。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-118">Use thumbprint to look up in the certificate in the store and sign in with that certificate.</span></span>

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a><span data-ttu-id="5a8b9-119">Universal Windows Platform アプリの署名にセキュリティで保護されたファイル タスクを使用する</span><span class="sxs-lookup"><span data-stu-id="5a8b9-119">Use a Secure File task for Universal Windows Platform app signing</span></span>

<span data-ttu-id="5a8b9-120">セキュリティで保護されたファイル タスクの使用は、Universal Windows Platform (UWP) アプリの署名に推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-120">Using a Secure File task is the recommended approach for Universal Windows Platform (UWP) app signing.</span></span> <span data-ttu-id="5a8b9-121">パッケージ署名の詳細については、[パッケージ署名の構成](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-121">For more information about package signing, see [Configure package signing](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing).</span></span> <span data-ttu-id="5a8b9-122">このプロセスを次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-122">This process is shown in the following image.</span></span>

![MPOS アプリ署名フロー](media/POSSigningFlow.png)

## <a name="steps-to-configure-the-certificate-for-signing"></a><span data-ttu-id="5a8b9-124">署名のために証明書を構成する手順</span><span class="sxs-lookup"><span data-stu-id="5a8b9-124">Steps to configure the certificate for signing</span></span>

### <a name="certificate-in-the-file-systemsecure-location"></a><span data-ttu-id="5a8b9-125">ファイル システム / 安全な場所の証明書</span><span class="sxs-lookup"><span data-stu-id="5a8b9-125">Certificate in the file system/secure location</span></span>

<span data-ttu-id="5a8b9-126">[ダウンロードファイル タスク](https://docs.microsoft.com/visualstudio/msbuild/downloadfile-task?view=vs-2019)をダウンロードして、ビルド プロセスの最初の手順として追加します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-126">Download the [DownloadFile task](https://docs.microsoft.com/visualstudio/msbuild/downloadfile-task?view=vs-2019) and add it as the first step in the build process.</span></span> <span data-ttu-id="5a8b9-127">セキュリティで保護されたファイルのタスクを使用する利点は、ビルド パイプラインが成功したか、失敗したか、またはキャンセルされたかに関係なく、ビルド時にファイルが暗号化されてディスクに格納されることです。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-127">The advantage of using the Secure File task is that the file is encrypted and placed in the disk during build no matter if the build pipeline succeeds, fails, or is canceled.</span></span> <span data-ttu-id="5a8b9-128">このファイルは、ビルド プロセスの完了後にダウンロード場所から削除されます。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-128">The file is deleted from the download location after the build process is completed.</span></span>

1. <span data-ttu-id="5a8b9-129">Azure DevOps ビルド パイプラインの最初のステップとして、セキュア ファイル タスクをダウンロードして追加します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-129">Download and add the Secure File task as the first step in the Azure DevOps build pipeline.</span></span> <span data-ttu-id="5a8b9-130">セキュア ファイル タスクは、[DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-130">You can download the Secure File task from [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).</span></span>
2. <span data-ttu-id="5a8b9-131">次の図に示すように、証明書をセキュア ファイル タスクにアップロードし、出力変数で参照名を設定します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-131">Upload the certificate to the Secure File task and set the Reference name under Output Variables, as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="5a8b9-132">![セキュア ファイル タスク](media/SecureFile.png)</span><span class="sxs-lookup"><span data-stu-id="5a8b9-132">![Secure file task](media/SecureFile.png)</span></span>
3. <span data-ttu-id="5a8b9-133">**変数**タブの下の**新しい変数**をクリックして、Azure DevOps パイプラインに新しい変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-133">Create a new variable in the Azure DevOps pipeline by clicking **New Variable** under the **Variables** tab.</span></span>
4. <span data-ttu-id="5a8b9-134">値フィールド **$(MySigningCert.secureFilePath)** に、**CertFile** などの変数の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-134">Provide a name for the variable in the value field **$(MySigningCert.secureFilePath)**, for example, **CertFile**.</span></span>
5. <span data-ttu-id="5a8b9-135">変数を保存します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-135">Save the variable.</span></span>
6. <span data-ttu-id="5a8b9-136">**RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、**ModernPOSPackageCertificateKeyFile** を Azure DevOps パイプラインで作成された変数で更新します (手順 3)。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-136">Open the **Customization.settings** file from **RetailSDK\\BuildTools** and update the **ModernPOSPackageCertificateKeyFile** with the variable name created in the Azure DevOps pipeline (step 3).</span></span> <span data-ttu-id="5a8b9-137">例:</span><span class="sxs-lookup"><span data-stu-id="5a8b9-137">For example:</span></span>
    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(CertFile</ModernPOSPackageCertificateKeyFile>
    ```

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app"></a><span data-ttu-id="5a8b9-138">MPOS アプリに署名するために証明書をダウンロードまたは生成する</span><span class="sxs-lookup"><span data-stu-id="5a8b9-138">Download or generate a certificate to sign the MPOS app</span></span>

<span data-ttu-id="5a8b9-139">ダウンロードまたは生成された証明書を使用して MPOS アプリに署名する場合、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateKeyFile** ノードを更新して、pfx ファイルの場所 (**$(SdkReferencesPath)\\appxsignkey.pfx**) を指すようにします。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-139">If a downloaded or generated certificate is used to sign the MPOS app, then the update the **ModernPOSPackageCertificateKeyFile** node in the **BuildTools\\Customization.settings** file to point to the pfx file location (**$(SdkReferencesPath)\\appxsignkey.pfx**).</span></span> <span data-ttu-id="5a8b9-140">例:</span><span class="sxs-lookup"><span data-stu-id="5a8b9-140">For example:</span></span>

<span data-ttu-id="5a8b9-141"><ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile></span><span class="sxs-lookup"><span data-stu-id="5a8b9-141"><ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile></span></span>

<span data-ttu-id="5a8b9-142">この場合、証明書ファイル名は **appxsignkey.pfx** であり、**Retail SDK\\ 参照**フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-142">In this case, the certificate file name is **appxsignkey.pfx**, located in the **Retail SDK\\Reference** folder.</span></span>

## <a name="use-thumbprint-to-sign-the-mpos-app"></a><span data-ttu-id="5a8b9-143">拇印を使用して MPOS アプリに署名する</span><span class="sxs-lookup"><span data-stu-id="5a8b9-143">Use thumbprint to sign the MPOS app</span></span>

<span data-ttu-id="5a8b9-144">拇印を使用して MPOS アプリに署名する場合は、証明書をローカルにインストールします。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-144">If you use thumbprint to sign the MPOS app, then install the certificate locally.</span></span> <span data-ttu-id="5a8b9-145">**BuildTools\\Customization.settings** ファイルにある **ModernPOSPackageCertificateThumbprint** ノードで、拇印の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-145">Update the thumbprint value in the **ModernPOSPackageCertificateThumbprint** node in the **BuildTools\\Customization.settings** file.</span></span>

<span data-ttu-id="5a8b9-146">このオプションは、ビルド ユーザーがローカル ユーザーの場合に機能します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-146">This option will work if the build user is a local user.</span></span> <span data-ttu-id="5a8b9-147">ただし、Azure DevOps/Visual Studio Online エージェントを使用してビルドを生成している場合、エージェントは証明書ストアにアクセスして署名に証明書を使用する権限を持たないか、ビルド マシンに証明書がインストールされない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-147">However if you are using the Azure DevOps/Visual Studio Online agents to generate the build, then the agent may not have permission to access the cert store to use the certificate for signing or the build machine will not have the certificate installed.</span></span> <span data-ttu-id="5a8b9-148">この場合、ビルド ユーザーをローカル ユーザーに変更し、そのボックスに証明書をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-148">In this case, the workaround is to change the build user to local user and install the certificate in the box.</span></span> <span data-ttu-id="5a8b9-149">ただし、ボックスへの管理者アクセス権限がない場合は、このオプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-149">However, this option will not work if you don’t have admin access to the box.</span></span>

> [!NOTE]
> <span data-ttu-id="5a8b9-150">pfx file またはセキュア ファイル タスク オプションを使用してアプリに署名する場合は、**Customization.settings** ファイルの **ModernPOSPackageCertificateThumbprint**ノードを空のままにします。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-150">If the .pfx file or Secure File task option is used to sign the app, then leave the **ModernPOSPackageCertificateThumbprint** node in the **Customization.settings** file empty.</span></span> <span data-ttu-id="5a8b9-151">拇印オプションが使用されている場合、**ModernPOSPackageCertificateKeyFile** を空のままにします。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-151">If the thumbprint option is used, then leave **ModernPOSPackageCertificateKeyFile** empty.</span></span> <span data-ttu-id="5a8b9-152">両方の値を更新すると、ビルドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-152">If both the values are updated, then the build will fail.</span></span>
