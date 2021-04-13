---
title: コード署名証明書を使用して MPOS に署名する
description: このトピックでは、コード署名証明書を使用して MPOS に署名する方法について説明します。
author: mugunthanm
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 35623a1ed24859a326ac901f2c8dbb5dcc8dd6c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791151"
---
# <a name="sign-mpos-appx-with-a-code-signing-certificate"></a><span data-ttu-id="86ecb-103">コード署名証明書を使用した MPOS appx の署名</span><span class="sxs-lookup"><span data-stu-id="86ecb-103">Sign MPOS appx with a code signing certificate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86ecb-104">Modern POS (MPOS) をインストールするには、信頼されたプロバイダーからのコード署名証明書を使用して MPOS アプリに署名し、現在のユーザーの信頼されたルート フォルダーの下に MPOS がインストールされているすべてのコンピューターに同じ証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-104">To install Modern POS (MPOS) you must sign the MPOS app with a code signing certificate from a trusted provider and install the same certificate on all the machines where MPOS is installed under the trusted root folder for the current user.</span></span>

<span data-ttu-id="86ecb-105">証明書を使用して MPOS アプリに署名するために、**Retail SDK\\ビルド ツール\\Customization.settings** ファイルにあるオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-105">To sign the MPOS app with a certificate, use one of these options in the **Retail SDK\\Build tool\\Customization.settings** file:</span></span>

- <span data-ttu-id="86ecb-106">Azure DevOps ビルド ステップのセキュア ファイル タスク部分を追加して、証明書をアップロードしてファイル タスクを保護します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-106">Add the Secure file task part of Azure DevOps build steps and upload the certificate to secure the file task.</span></span> <span data-ttu-id="86ecb-107">セキュア ファイル タスクの出力パス変数を Customization.settings ファイルのパラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-107">Use the secure file task output path variable as a parameter in the Customization.settings file.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86ecb-108">セキュリティで保護されたファイル タスクは、パスワードで保護された証明書をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="86ecb-108">The Secure File task doesn’t support a password protected certificate.</span></span> <span data-ttu-id="86ecb-109">このタスクをアップロードする前にパスワードを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-109">You must remove the password before uploading this task.</span></span> <span data-ttu-id="86ecb-110">証明書は、Azure のセキュリティで保護されたファイル システム タスクにアップロードされるため、このステップのパスワードのみを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-110">Because the certificate is uploaded to the secure file system task in Azure, you can remove the password only for this step.</span></span> <span data-ttu-id="86ecb-111">ただし、パスワードの削除についてはセキュリティの専門家と話し合って、これがプロジェクトにとって正しいアクションであるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-111">However, you should discuss removing the password with your security experts to determine if this is the correct action for your project.</span></span> <span data-ttu-id="86ecb-112">他のシナリオの証明書のパスワードは削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="86ecb-112">Don’t remove the certificate password for other scenarios.</span></span>
- <span data-ttu-id="86ecb-113">ファイル システムにある証明書を使用してください。</span><span class="sxs-lookup"><span data-stu-id="86ecb-113">Use a certificate that is in the file system.</span></span> <span data-ttu-id="86ecb-114">これを行うには、証明書をダウンロードまたは生成し、ビルドが実行されているファイル システムに配置します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-114">To do this, download or generate a certificate and place it in the file system where the build is running.</span></span> <span data-ttu-id="86ecb-115">Microsoft にホストされるエージェントまたはビルド ユーザーは、このパスとファイルへのアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="86ecb-115">The Microsoft-hosted agent or build user should have access to this path and file.</span></span>
- <span data-ttu-id="86ecb-116">拇印を使用してストア内の証明書を検索し、その証明書でサインインします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-116">Use thumbprint to look up in the certificate in the store and sign in with that certificate.</span></span>

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a><span data-ttu-id="86ecb-117">Universal Windows Platform アプリの署名にセキュリティで保護されたファイル タスクを使用する</span><span class="sxs-lookup"><span data-stu-id="86ecb-117">Use a Secure File task for Universal Windows Platform app signing</span></span>

<span data-ttu-id="86ecb-118">セキュリティで保護されたファイル タスクの使用は、Universal Windows Platform (UWP) アプリの署名に推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="86ecb-118">Using a Secure File task is the recommended approach for Universal Windows Platform (UWP) app signing.</span></span> <span data-ttu-id="86ecb-119">パッケージ署名の詳細については、[パッケージ署名の構成](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86ecb-119">For more information about package signing, see [Configure package signing](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing).</span></span> <span data-ttu-id="86ecb-120">このプロセスを次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-120">This process is shown in the following image.</span></span>

![MPOS アプリ署名フロー](media/POSSigningFlow.png)

> [!NOTE]
> <span data-ttu-id="86ecb-122">現在 OOB パッケージでは、appx ファイルの署名のみがサポートされており、MPOIS、RSSU、HWSなどのセルフ サービスの他のインストーラーは、このプロセスによって署名されません。</span><span class="sxs-lookup"><span data-stu-id="86ecb-122">Currently the OOB packaging supports signing only the appx file, the different self-service installers like MPOIS, RSSU, and HWS are not signed by this process.</span></span> <span data-ttu-id="86ecb-123">SignTool またはその他の署名ツールを使用して、手動で署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-123">You need to manually sign it using SignTool or other signing tools.</span></span> <span data-ttu-id="86ecb-124">appx ファイルの署名に使用する証明書は、Modern POS がインストールされているマシンにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-124">The certificate used for signing the appx file must be installed in the machine where Modern POS is installed.</span></span>

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a><span data-ttu-id="86ecb-125">Azure Pipelines にサインインするための証明書を構成する手順</span><span class="sxs-lookup"><span data-stu-id="86ecb-125">Steps to configure the certificate for signing in Azure Pipelines</span></span>

### <a name="certificate-in-the-file-systemsecure-location"></a><span data-ttu-id="86ecb-126">ファイル システム / 安全な場所の証明書</span><span class="sxs-lookup"><span data-stu-id="86ecb-126">Certificate in the file system/secure location</span></span>

<span data-ttu-id="86ecb-127">[ダウンロードファイル タスク](https://docs.microsoft.com/visualstudio/msbuild/downloadfile-task)をダウンロードして、ビルド プロセスの最初の手順として追加します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-127">Download the [DownloadFile task](https://docs.microsoft.com/visualstudio/msbuild/downloadfile-task) and add it as the first step in the build process.</span></span> <span data-ttu-id="86ecb-128">セキュリティで保護されたファイルのタスクを使用する利点は、ビルド パイプラインが成功したか、失敗したか、またはキャンセルされたかに関係なく、ビルド時にファイルが暗号化されてディスクに格納されることです。</span><span class="sxs-lookup"><span data-stu-id="86ecb-128">The advantage of using the Secure File task is that the file is encrypted and placed in the disk during build no matter if the build pipeline succeeds, fails, or is canceled.</span></span> <span data-ttu-id="86ecb-129">このファイルは、ビルド プロセスの完了後にダウンロード場所から削除されます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-129">The file is deleted from the download location after the build process is completed.</span></span>

1. <span data-ttu-id="86ecb-130">最初のステップとして、Azure ビルド パイプラインでセキュア ファイル タスクをダウンロードして追加します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-130">Download and add the Secure File task as the first step in the Azure build pipeline.</span></span> <span data-ttu-id="86ecb-131">セキュア ファイル タスクは、[DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-131">You can download the Secure File task from [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).</span></span>
2. <span data-ttu-id="86ecb-132">次の図に示すように、証明書をセキュア ファイル タスクにアップロードし、出力変数で参照名を設定します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-132">Upload the certificate to the Secure File task and set the Reference name under Output Variables, as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="86ecb-133">![セキュア ファイル タスク](media/SecureFile.png)</span><span class="sxs-lookup"><span data-stu-id="86ecb-133">![Secure file task](media/SecureFile.png)</span></span>
3. <span data-ttu-id="86ecb-134">**変数** タブの下の **新しい変数** を選択して、Azure Pipelines に新しい変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-134">Create a new variable in Azure Pipelines by selecting **New Variable** under the **Variables** tab.</span></span>
4. <span data-ttu-id="86ecb-135">値フィールドに変数の名前を入力します (例: **MySigningCert**)。</span><span class="sxs-lookup"><span data-stu-id="86ecb-135">Provide a name for the variable in the value field, for example, **MySigningCert**.</span></span>
5. <span data-ttu-id="86ecb-136">変数を保存します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-136">Save the variable.</span></span>
6. <span data-ttu-id="86ecb-137">**RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、パイプラインで作成された変数名で **ModernPOSPackageCertificateKeyFile** を更新します (手順 3)。</span><span class="sxs-lookup"><span data-stu-id="86ecb-137">Open the **Customization.settings** file from **RetailSDK\\BuildTools** and update the **ModernPOSPackageCertificateKeyFile** with the variable name created in the pipeline (step 3).</span></span> <span data-ttu-id="86ecb-138">例:</span><span class="sxs-lookup"><span data-stu-id="86ecb-138">For example:</span></span>

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    <span data-ttu-id="86ecb-139">証明書がパスワードで保護されていない場合は、この手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-139">This step is required if the certificate is not password protected.</span></span> <span data-ttu-id="86ecb-140">証明書がパスワードで保護されている場合は、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-140">If the certificate is password protected, continue with the following steps.</span></span>
 
7. <span data-ttu-id="86ecb-141">パイプラインの **変数** タブで、セキュリティで保護された新しいテキスト変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-141">On the pipeline’s **Variables** tab, add a new secure-text variable.</span></span> <span data-ttu-id="86ecb-142">名前を **MySigningCert.secret** に設定し、証明書のパスワードの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-142">Set the name to **MySigningCert.secret** and set the value of the password for the certificate.</span></span> <span data-ttu-id="86ecb-143">変数を保護するには、ロック アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-143">Select the lock icon to secure the variable.</span></span>
8. <span data-ttu-id="86ecb-144">**Powershell スクリプト** タスクをパイプラインに追加します (セキュリティで保護されたファイルのダウンロード後、およびビルド ステップの前)。</span><span class="sxs-lookup"><span data-stu-id="86ecb-144">Add a **Powershell Script** task to the pipeline (after the Download Secure File and before the Build step).</span></span> <span data-ttu-id="86ecb-145">**表示** 名を指定し、タイプを **インライン** として設定します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-145">Provide the **Display** name and set the Type as **Inline**.</span></span> <span data-ttu-id="86ecb-146">以下をコピーしてスクリプト セクションに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-146">Copy and paste the following into the script section.</span></span>

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

9. <span data-ttu-id="86ecb-147">**RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、**ModernPOSPackageCertificateThumbprint** を証明書の拇印の値で更新します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-147">Open the **Customization.settings** file from **RetailSDK\\BuildTools** and update the **ModernPOSPackageCertificateThumbprint** with the certificate thumbprint value.</span></span>

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a><span data-ttu-id="86ecb-148">SDK の msbuild を使用して手動で MPOS アプリに署名する証明書をダウンロードまたは生成する</span><span class="sxs-lookup"><span data-stu-id="86ecb-148">Download or generate a certificate to sign the MPOS app manually using msbuild in SDK</span></span>

<span data-ttu-id="86ecb-149">ダウンロードまたは生成された証明書を使用して MPOS アプリに署名する場合、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateKeyFile** ノードを更新して、pfx ファイルの場所 (**$(SdkReferencesPath)\\appxsignkey.pfx**) を指すようにします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-149">If a downloaded or generated certificate is used to sign the MPOS app, then the update the **ModernPOSPackageCertificateKeyFile** node in the **BuildTools\\Customization.settings** file to point to the pfx file location (**$(SdkReferencesPath)\\appxsignkey.pfx**).</span></span> <span data-ttu-id="86ecb-150">例:</span><span class="sxs-lookup"><span data-stu-id="86ecb-150">For example:</span></span>

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

<span data-ttu-id="86ecb-151">この場合、証明書ファイル名は **appxsignkey.pfx** であり、**Retail SDK\\ 参照** フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-151">In this case, the certificate file name is **appxsignkey.pfx**, located in the **Retail SDK\\Reference** folder.</span></span>

## <a name="use-thumbprint-to-sign-the-mpos-app"></a><span data-ttu-id="86ecb-152">拇印を使用して MPOS アプリに署名する</span><span class="sxs-lookup"><span data-stu-id="86ecb-152">Use thumbprint to sign the MPOS app</span></span>

<span data-ttu-id="86ecb-153">拇印を使用して MPOS アプリに署名する場合は、証明書をローカルにインストールします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-153">If you use thumbprint to sign the MPOS app, then install the certificate locally.</span></span> <span data-ttu-id="86ecb-154">**BuildTools\\Customization.settings** ファイルにある **ModernPOSPackageCertificateThumbprint** ノードで、拇印の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-154">Update the thumbprint value in the **ModernPOSPackageCertificateThumbprint** node in the **BuildTools\\Customization.settings** file.</span></span>

<span data-ttu-id="86ecb-155">このオプションは、ビルド ユーザーがローカル ユーザーの場合に機能します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-155">This option will work if the build user is a local user.</span></span> <span data-ttu-id="86ecb-156">ただし、Azure DevOps エージェントを使用してビルドを生成している場合、エージェントは証明書ストアにアクセスして署名に証明書を使用する権限を持たないので、ビルド マシンに証明書がインストールされない可能性があります。　</span><span class="sxs-lookup"><span data-stu-id="86ecb-156">However if you are using the Azure DevOps agents to generate the build, then the agent may not have permission to access the cert store to use the certificate for signing or the build machine will not have the certificate installed.</span></span> <span data-ttu-id="86ecb-157">この場合、ビルド ユーザーをローカル ユーザーに変更し、そのボックスに証明書をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-157">In this case, the workaround is to change the build user to local user and install the certificate in the box.</span></span> <span data-ttu-id="86ecb-158">ただし、ボックスへの管理者アクセス権限がない場合は、このオプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="86ecb-158">However, this option will not work if you don’t have admin access to the box.</span></span>

> [!NOTE]
> <span data-ttu-id="86ecb-159">pfx file またはセキュア ファイル タスク オプションを使用してアプリに署名する場合は、**Customization.settings** の **ModernPOSPackageCertificateThumbprint** ノードを空のままにします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-159">If the .pfx file or Secure File task option is used to sign the app, then leave the **ModernPOSPackageCertificateThumbprint** node in **Customization.settings** empty.</span></span> <span data-ttu-id="86ecb-160">拇印オプションが使用されている場合、**ModernPOSPackageCertificateKeyFile** を空のままにします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-160">If the thumbprint option is used, then leave **ModernPOSPackageCertificateKeyFile** empty.</span></span> <span data-ttu-id="86ecb-161">両方の値を更新すると、ビルドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-161">If both the values are updated, then the build will fail.</span></span>

### <a name="certification-renewal"></a><span data-ttu-id="86ecb-162">証明書の更新</span><span class="sxs-lookup"><span data-stu-id="86ecb-162">Certification renewal</span></span>

### <a name="renew-a-certificate-from-trusted-ca"></a><span data-ttu-id="86ecb-163">信頼される CA から証明書を更新する</span><span class="sxs-lookup"><span data-stu-id="86ecb-163">Renew a certificate from trusted CA</span></span>

<span data-ttu-id="86ecb-164">証明書の更新プロセスについては、証明機関 (CA) に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="86ecb-164">Contact your certifying authority (CA) for the certificate renewal process.</span></span> <span data-ttu-id="86ecb-165">信頼される証明書については、MPOS 側でアクションを実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="86ecb-165">For a trusted certificate, no action is required on the MPOS side.</span></span>

### <a name="renew-a-self-signed-certificate"></a><span data-ttu-id="86ecb-166">自己署名証明書を更新する</span><span class="sxs-lookup"><span data-stu-id="86ecb-166">Renew a self-signed certificate</span></span>

<span data-ttu-id="86ecb-167">実稼働用の Retail SDK で使用可能なサンプル証明書は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="86ecb-167">Don’t use the sample certificate available in the Retail SDK for production.</span></span> <span data-ttu-id="86ecb-168">開発の目的にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-168">It can be used only for development purposes.</span></span> <span data-ttu-id="86ecb-169">サンプルの Contoso の証明書は更新することができず、10.0.16 またはそれ以前のバージョンの Retail SDK に含まれているサンプルの証明書は、2020 年 12 月 31 日に有効期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-169">The sample Contoso certificate can't be renewed and the sample certificate included in Retail SDK version 10.0.16 or earlier will expire on December 31, 2020.</span></span> <span data-ttu-id="86ecb-170">カスタマイズされた Modern POS に署名するためにこの証明書または自己署名証明書を使用した場合、この日付の後は Modern POS が正しく機能しなくなる可能性が大いにあります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-170">If this certificate, or a self-signed certificate, has been used to sign a customized Modern POS, there is a strong possibility that Modern POS will not function properly after this  date.</span></span>
 
### <a name="impact"></a><span data-ttu-id="86ecb-171">影響</span><span class="sxs-lookup"><span data-stu-id="86ecb-171">Impact</span></span>
 
<span data-ttu-id="86ecb-172">上記の場合、2020 年 12 月 31 日以降はインストーラーを実行できないという問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-172">If the above is true for you, the issue you will be encountering is that the installer will not be able to run after December 31, 2020.</span></span> <span data-ttu-id="86ecb-173">使用している会社の IT ポリシーによっては、Modern POS が機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-173">Depending on the corporate IT policies used, Modern POS may not be able to function.</span></span> <span data-ttu-id="86ecb-174">組織への影響を判断するために、日付を一時的に未来の日付に変更してテストすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="86ecb-174">It is critical that you test this by changing the date temporarily to a future date, to determine the impact to your organization.</span></span>
 
### <a name="steps-to-determine-the-issue"></a><span data-ttu-id="86ecb-175">問題を特定する手順</span><span class="sxs-lookup"><span data-stu-id="86ecb-175">Steps to determine the issue</span></span>
 
1.  <span data-ttu-id="86ecb-176">Windows の設定を使用して、コンピュータの日時を 2021 年の時刻に変更します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-176">Use Windows settings to change the computer clock to a date and time in the year 2021.</span></span>
2.  <span data-ttu-id="86ecb-177">Modern POS を開くことができることを確認し、サインインを実行すると、トランザクションを完了することができます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-177">Verify that Modern POS can be opened, sign in can occur, and a transaction can be completed.</span></span>
3.  <span data-ttu-id="86ecb-178">Modern POS のセルフ サービス インストーラーが実行可能であることを確認します。実行可能な場合、インストールは正常に完了します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-178">Verify that Modern POS Self-service installer is able to be run, and if so, that installation will complete successfully.</span></span>
4.  <span data-ttu-id="86ecb-179">Windows の日時設定を正しい時刻に戻します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-179">Return the Windows clock settings to the correct date and time.</span></span>
 
<span data-ttu-id="86ecb-180">これらの手順すべてを問題なく完了できる場合、現在の証明書で 2020 年 12 月 31 日までの操作が可能になります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-180">If you can complete all of these steps without issues, then you will be able to operate on the current certificate past December 31, 2020.</span></span>  
 
### <a name="steps-going-forward"></a><span data-ttu-id="86ecb-181">今後の手順</span><span class="sxs-lookup"><span data-stu-id="86ecb-181">Steps going forward</span></span> 

<span data-ttu-id="86ecb-182">以前に使用していた証明書を更新することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-182">It is highly recommended that you renew the previously used certificate.</span></span> <span data-ttu-id="86ecb-183">新しい証明書を取得することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="86ecb-183">We strongly recommend that you obtain a new certificate.</span></span> <span data-ttu-id="86ecb-184">これを実行するには、次のアクションのいずれかを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-184">To do this, you must perform one of the following actions:</span></span>
 
- <span data-ttu-id="86ecb-185">**優先** - 信頼される証明機関からコード署名証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-185">**Preferred** - Obtain a code signing certificate from a trusted certificate authority.</span></span>

- <span data-ttu-id="86ecb-186">**優先** - 使用する自己署名のコード署名証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-186">**Preferred** - Generate a self-signed code signing certificate to use.</span></span> <span data-ttu-id="86ecb-187">通常、これはドメイン内で使用されます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-187">This is typically used when within a domain.</span></span>

- <span data-ttu-id="86ecb-188">**一時的なソリューションとして利用可能** - 更新された Contoso のコード署名証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-188">**Available as a temporary Solution** - Use the renewed Contoso code signing certificate.</span></span> <span data-ttu-id="86ecb-189">通常、これはテスト目的で使用されるため、運用環境に配置することはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="86ecb-189">This is typically used for testing purposes, so it's not recommended that it be deployed in production.</span></span>
 
<span data-ttu-id="86ecb-190">次に、上記のいずれかのアクションから取得した証明書を使用して署名された、新しくカスタマイズされた Modern POS のパッケージを生成します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-190">Next, generate a new customized Modern POS package that is signed using this certificate obtained from one of the actions above.</span></span> <span data-ttu-id="86ecb-191">証明書に応じて、次のいずれかの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="86ecb-191">Depending on the certificate, one of the following steps must be followed:</span></span>
 
- <span data-ttu-id="86ecb-192">新しい信頼される証明書 (または新しい自己署名の証明書) を使用する場合、すべてのデバイスに新しい証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-192">If using a new, trusted certificate (or a new, self-signed certificate), you will be  required to install a new certificate on every device.</span></span> <span data-ttu-id="86ecb-193">その後、新しく作成された Modern POS のパッケージ (インストーラー) を使用して、既存のアプリケーションをアンインストールし、新しい Modern POS パッケージを再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-193">After that, you need to take the newly created Modern POS Package (installer), uninstall the existing application, and then reinstall the new Modern POS package.</span></span> <span data-ttu-id="86ecb-194">すべてのデバイスで Modern POS のデバイスの有効化を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-194">You will need to perform a device activation of Modern POS on every device.</span></span>

- <span data-ttu-id="86ecb-195">更新された Contoso 証明書を使用する場合、すべてのデバイスに新しい証明書をインストールして、Modern POS パッケージ (インストーラー) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-195">If using the renewed Contoso certificate, you will be required to install the new certificate on every device and install the Modern POS Package (installer).</span></span> <span data-ttu-id="86ecb-196">アンインストールする必要はありませんが、デバイスに再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86ecb-196">You are not required to uninstall, however you must reinstall on the device.</span></span> <span data-ttu-id="86ecb-197">Modern POS のデバイスの有効化は必須ではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="86ecb-197">Note that device activation of Modern POS will not be required.</span></span> <span data-ttu-id="86ecb-198">このオプションは一時的なソリューションです。</span><span class="sxs-lookup"><span data-stu-id="86ecb-198">This option is a temporary solution.</span></span> <span data-ttu-id="86ecb-199">新しい信頼される証明書を取得する前にこのオプションを使用するだけで最有効化を回避し、問題を解決することができます。</span><span class="sxs-lookup"><span data-stu-id="86ecb-199">Only use this option to avoid reactivation and resolve the issue before obtaining a new trusted certificate.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
