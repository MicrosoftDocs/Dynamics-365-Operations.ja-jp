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
ms.openlocfilehash: efb1ba4d890cbf02296994179efd8198a306505f
ms.sourcegitcommit: 2555acfd855fc18ff3ba432ba2cf7633a8f1653c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2019
ms.locfileid: "2238561"
---
# <a name="sign-mpos-with-a-code-signing-certificate"></a><span data-ttu-id="b82e3-103">コード署名証明書を使用して MPOS に署名する</span><span class="sxs-lookup"><span data-stu-id="b82e3-103">Sign MPOS with a code signing certificate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b82e3-104">Windows に Modern POS (MPOS) をインストールするには、信頼されたプロバイダーからの署名証明書を使用して MPOS アプリに署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b82e3-104">To install Modern POS (MPOS) in Windows you must sign the MPOS app with a signing certificate from a trusted provider.</span></span> <span data-ttu-id="b82e3-105">証明書を使用して MPOS アプリに署名するためのオプションが以下の場所にいくつかあります **Retail SDK\\ビルド ツール\\Customization.settings** ファイル:</span><span class="sxs-lookup"><span data-stu-id="b82e3-105">To sign the MPOS app with a certificate, there are these options in the **Retail SDK\\Build tool\\Customization.settings** file:</span></span>

- <span data-ttu-id="b82e3-106">Azure DevOps ビルド ステップのセキュリティで保護されたファイル タスク部分を追加し、証明書をアップロードしてファイル タスクをセキュリティ保護し、セキュリティで保護されたファイル タスクの出力パス変数を Customization.settings ファイルのパラメータとして使用します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-106">Add the Secure file task part of Azure DevOps build steps and upload the certificate to secure the file task and use the secure file task output path variable as parameter in the Customization.settings file.</span></span>
    > [!NOTE] 
    > <span data-ttu-id="b82e3-107">セキュリティで保護されたファイル タスクは、パスワードで保護された証明書をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b82e3-107">The Secure file task doesn’t support password protected certificate.</span></span> <span data-ttu-id="b82e3-108">このタスクにアップロードする前にパスワードを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b82e3-108">You must remove the password before uploading to this task.</span></span> <span data-ttu-id="b82e3-109">証明書は、Microsoft Azure のセキュリティで保護されたファイル システム タスクにアップロードされるため、このステップのパスワードのみを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="b82e3-109">Because the certificate is uploaded to the secure file system task in Microsoft Azure, it's okay to remove the password only for this step.</span></span> <span data-ttu-id="b82e3-110">パスワードの削除についてセキュリティの専門家と話し合って、これがプロジェクトにとって正しいアクションであるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b82e3-110">You must discuss removing the password with your security experts to determine if this is the correct action for your project.</span></span> <span data-ttu-id="b82e3-111">ビルド タスクにアップロードされた証明書は、ビルド フロー中にビルド パイプラインによってのみアクセスできます。他のプロセスがアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b82e3-111">The certificate uploaded to the build task can be accessed only by the build pipeline during the build flow and no other process can access it.</span></span> <span data-ttu-id="b82e3-112">セキュリティで保護されたファイル タスクを使用すると、ビルド署名プロセス中にパスワード セキュリティの追加レイヤーは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b82e3-112">With secure file task, the additional layer of password security is not required during the build signing process.</span></span> <span data-ttu-id="b82e3-113">他のシナリオの証明書のパスワードは削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="b82e3-113">Do not remove the certificate password for other scenarios.</span></span>
- <span data-ttu-id="b82e3-114">ファイル システムに配置された証明書を使用します。証明書をダウンロードまたは生成し、ビルドを実行しているファイル システムに配置します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-114">Use a certificate placed in the file system: You download or generate a certificate and place it in the file system where the build is running.</span></span> <span data-ttu-id="b82e3-115">VSO エージェントまたはビルド ユーザーは、このパスとファイルにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b82e3-115">The VSO agent or build user should have access to this path and file.</span></span>
- <span data-ttu-id="b82e3-116">拇印を使用してストア内の証明書を検索し、その証明書で署名します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-116">Use thumbprint to look up in the certificate in the store and sign with that certificate.</span></span>

## <a name="using-a-secure-file-task-is-the-recommended-approach-for-uwp-app-signing"></a><span data-ttu-id="b82e3-117">セキュリティで保護されたファイル タスクの使用は、UWP アプリの署名に推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="b82e3-117">Using a Secure File task is the recommended approach for UWP app signing</span></span>

<span data-ttu-id="b82e3-118">パッケージ署名については、[パッケージ署名の構成](https://docs.microsoft.com/en-us/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b82e3-118">For information on package signing, see [Configure package signing](https://docs.microsoft.com/en-us/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing).</span></span> <span data-ttu-id="b82e3-119">プロセスを次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-119">The process is shown in the following image:</span></span>

![MPOS アプリ署名フロー](media/POSSigningFlow.png)

## <a name="steps-to-configure-the-certificate-for-signing"></a><span data-ttu-id="b82e3-121">署名のために証明書を構成する手順</span><span class="sxs-lookup"><span data-stu-id="b82e3-121">Steps to configure the certificate for signing</span></span>

### <a name="certificate-in-the-file-systemsecure-location"></a><span data-ttu-id="b82e3-122">ファイル システム / 安全な場所の証明書:</span><span class="sxs-lookup"><span data-stu-id="b82e3-122">Certificate in the file system/secure location:</span></span>

<span data-ttu-id="b82e3-123">[ファイル タスクをダウンロード](https://docs.microsoft.com/en-us/visualstudio/msbuild/downloadfile-task?view=vs-2019)して、ビルド プロセスの最初の手順として追加します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-123">Download the [Download File task](https://docs.microsoft.com/en-us/visualstudio/msbuild/downloadfile-task?view=vs-2019) and add it as first step in the build process.</span></span> <span data-ttu-id="b82e3-124">セキュア ファイル タスクを使用する利点は、ビルド中にファイルが暗号化されてディスクに配置されることであり、ビルド パイプラインが成功、失敗、またはキャンセルされたかどうかに関係なく、ファイルはビルド プロセスの完了後にダウンロード場所から削除されます。</span><span class="sxs-lookup"><span data-stu-id="b82e3-124">The advantage of using the Secure File task is the file is encrypted and placed in the disk during build and no matter whether the build pipelines succeeds, fails, or canceled, the file is deleted from its download location after the build process is completed.</span></span>

1. <span data-ttu-id="b82e3-125">Azure DevOps ビルド パイプラインの最初のステップとして、セキュア ファイル タスクをダウンロードして追加します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-125">Download and add the Secure File task as first step in the Azure DevOps build pipeline.</span></span> <span data-ttu-id="b82e3-126">セキュア ファイル タスクは、 [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b82e3-126">You can download the secure file task from [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).</span></span>
2. <span data-ttu-id="b82e3-127">次の図に示すように、証明書をセキュア ファイル タスクにアップロードし、出力変数で参照名を設定します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-127">Upload the certificate to the Secure File task and set the Reference name under Output Variables, as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b82e3-128">![セキュア ファイル タスク](media/SecureFile.png)</span><span class="sxs-lookup"><span data-stu-id="b82e3-128">![Secure file task](media/SecureFile.png)</span></span>
3. <span data-ttu-id="b82e3-129">**変数**タブの下の**新しい変数**ボタンをクリックして、Azure DevOps に新しい変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-129">Create a new variable in the Azure DevOps pipeline by clicking the **New Variable** button under the **Variables** tab.</span></span>
4. <span data-ttu-id="b82e3-130">値フィールド **$(MySigningCert.secureFilePath)** に、**CertFile** などの変数の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-130">Provide a name for the variable, for example, **CertFile**, in the value field **$(MySigningCert.secureFilePath)**.</span></span>
5. <span data-ttu-id="b82e3-131">変数を保存します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-131">Save the variable.</span></span>
6. <span data-ttu-id="b82e3-132">**RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、**ModernPOSPackageCertificateKeyFile** を Azure DevOps パイプラインで作成された変数で更新します (手順 3)。</span><span class="sxs-lookup"><span data-stu-id="b82e3-132">Open the **Customization.settings** file from the **RetailSDK\\BuildTools** and update the **ModernPOSPackageCertificateKeyFile** with variable name created in the Azure DevOps pipeline (Step 3).</span></span> <span data-ttu-id="b82e3-133">例:</span><span class="sxs-lookup"><span data-stu-id="b82e3-133">For example:</span></span>
    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(CertFile</ModernPOSPackageCertificateKeyFile>
    ```

## <a name="downloaded-or-generated-certificate-to-sign-the-mpos-app"></a><span data-ttu-id="b82e3-134">MPOS アプリに署名するためにダウンロードまたは生成された証明書</span><span class="sxs-lookup"><span data-stu-id="b82e3-134">Downloaded or generated certificate to sign the MPOS app</span></span>

<span data-ttu-id="b82e3-135">ダウンロードまたは生成された証明書を使用して MPOS アプリに署名する場合、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateKeyFile** ノードを更新して、pfx ファイルの場所 (**$(SdkReferencesPath)\\appxsignkey.pfx**) を指すようにします。</span><span class="sxs-lookup"><span data-stu-id="b82e3-135">If a downloaded or generated certificate is used to sign the MPOS app then the update the **ModernPOSPackageCertificateKeyFile** node in the **BuildTools\\Customization.settings** file to point to the pfx file location (**$(SdkReferencesPath)\\appxsignkey.pfx**).</span></span> <span data-ttu-id="b82e3-136">例:</span><span class="sxs-lookup"><span data-stu-id="b82e3-136">For example:</span></span>

<span data-ttu-id="b82e3-137"><ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile></span><span class="sxs-lookup"><span data-stu-id="b82e3-137"><ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile></span></span>

<span data-ttu-id="b82e3-138">この場合、証明書ファイル名は **appxsignkey.pfx** であり、**Retail SDK\\参照**フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="b82e3-138">In this case the certificate file name is **appxsignkey.pfx** and it's placed in the **Retail SDK\\Reference** folder.</span></span>

## <a name="thumbprint-to-sign-the-mpos-app"></a><span data-ttu-id="b82e3-139">MPOS アプリに署名するための拇印</span><span class="sxs-lookup"><span data-stu-id="b82e3-139">Thumbprint to sign the MPOS app</span></span>

<span data-ttu-id="b82e3-140">拇印を使用して MPOS アプリに署名する場合、証明書をローカルにインストールし、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateThumbprint** ノードの拇印の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-140">If you use a thumbprint to sign the MPOS app then install the certificate locally and then update the thumbprint value in the **ModernPOSPackageCertificateThumbprint** node in the **BuildTools\\Customization.settings** file.</span></span>

<span data-ttu-id="b82e3-141">ビルド ユーザーがローカル ユーザーの場合、このオプションは正常に機能しますが、Azure DevOps/VSO エージェントを使用してビルドを生成している場合、エージェントは証明書ストアにアクセスして署名に証明書を使用する権限を持たないか、ビルド マシンに証明書がインストールされない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b82e3-141">This option will work fine if the build user is a local user but if you are using the Azure DevOps/VSO agents to generate the build then the agent may not have permission to access the cert store to use the certificate for signing or the build machine will not have the certificate installed.</span></span> <span data-ttu-id="b82e3-142">この場合の回避策は、ビルド ユーザーをローカル ユーザーに変更し、このボックスに証明書をインストールすることですが、このボックスに管理者としてアクセスする権限がない場合は、このオプションは正しく機能しません。</span><span class="sxs-lookup"><span data-stu-id="b82e3-142">The workaround in this case is change the build user to local user and install the certificate in the box but this option will not work well if you don’t have admin access to the box.</span></span>

> [!NOTE]
> <span data-ttu-id="b82e3-143">.pfx ファイルまたはセキュア ファイル タスク オプションを使用してアプリに署名する場合は、**Customization.settings** ファイルの **ModernPOSPackageCertificateThumbprint** ノードを空のままにし、拇印オプションを使用する場合は **ModernPOSPackageCertificateKeyFile** を空にします。</span><span class="sxs-lookup"><span data-stu-id="b82e3-143">If the .pfx file or Secure File task option is used to sign the app then leave the **ModernPOSPackageCertificateThumbprint** node in the **Customization.settings** file empty and if thumbprint option is used then leave the **ModernPOSPackageCertificateKeyFile** empty.</span></span> <span data-ttu-id="b82e3-144">両方の値を更新すると、ビルドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="b82e3-144">If both the values are updated, then the build will fail.</span></span>
