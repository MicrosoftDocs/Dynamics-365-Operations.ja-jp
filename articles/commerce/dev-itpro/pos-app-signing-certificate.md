---
title: コード署名証明書を使用して MPOS に署名する
description: このトピックでは、コード署名証明書を使用して MPOS に署名する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: aabca5d14e25069a9b34340e0e189223977e2348
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681528"
---
# <a name="sign-mpos-appx-with-a-code-signing-certificate"></a><span data-ttu-id="8b8a4-103">コード署名証明書を使用した MPOS appx の署名</span><span class="sxs-lookup"><span data-stu-id="8b8a4-103">Sign MPOS appx with a code signing certificate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b8a4-104">Modern POS (MPOS) をインストールするには、信頼されたプロバイダーからの署名証明書を使用して MPOS アプリに署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-104">To install Modern POS (MPOS) you must sign the MPOS app with a signing certificate from a trusted provider.</span></span> <span data-ttu-id="8b8a4-105">証明書を使用して MPOS アプリに署名するために、**Retail SDK\\ビルド ツール\\Customization.settings** ファイルにあるオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-105">To sign the MPOS app with a certificate, use one of these options in the **Retail SDK\\Build tool\\Customization.settings** file:</span></span>

- <span data-ttu-id="8b8a4-106">Azure DevOps ビルド ステップのセキュア ファイル タスク部分を追加して、証明書をアップロードしてファイル タスクを保護します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-106">Add the Secure file task part of Azure DevOps build steps and upload the certificate to secure the file task.</span></span> <span data-ttu-id="8b8a4-107">セキュア ファイル タスクの出力パス変数を Customization.settings ファイルのパラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-107">Use the secure file task output path variable as a parameter in the Customization.settings file.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b8a4-108">セキュリティで保護されたファイル タスクは、パスワードで保護された証明書をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-108">The Secure File task doesn’t support a password protected certificate.</span></span> <span data-ttu-id="8b8a4-109">このタスクをアップロードする前にパスワードを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-109">You must remove the password before uploading this task.</span></span> <span data-ttu-id="8b8a4-110">証明書は、Azure のセキュリティで保護されたファイル システム タスクにアップロードされるため、このステップのパスワードのみを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-110">Because the certificate is uploaded to the secure file system task in Azure, you can remove the password only for this step.</span></span> <span data-ttu-id="8b8a4-111">ただし、パスワードの削除についてはセキュリティの専門家と話し合って、これがプロジェクトにとって正しいアクションであるかどうかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-111">However, you should discuss removing the password with your security experts to determine if this is the correct action for your project.</span></span> <span data-ttu-id="8b8a4-112">他のシナリオの証明書のパスワードは削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-112">Don’t remove the certificate password for other scenarios.</span></span>
- <span data-ttu-id="8b8a4-113">ファイル システムにある証明書を使用してください。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-113">Use a certificate that is in the file system.</span></span> <span data-ttu-id="8b8a4-114">これを行うには、証明書をダウンロードまたは生成し、ビルドが実行されているファイル システムに配置します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-114">To do this, download or generate a certificate and place it in the file system where the build is running.</span></span> <span data-ttu-id="8b8a4-115">Microsoft にホストされるエージェントまたはビルド ユーザーは、このパスとファイルへのアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-115">The Microsoft-hosted agent or build user should have access to this path and file.</span></span>
- <span data-ttu-id="8b8a4-116">拇印を使用してストア内の証明書を検索し、その証明書でサインインします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-116">Use thumbprint to look up in the certificate in the store and sign in with that certificate.</span></span>

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a><span data-ttu-id="8b8a4-117">Universal Windows Platform アプリの署名にセキュリティで保護されたファイル タスクを使用する</span><span class="sxs-lookup"><span data-stu-id="8b8a4-117">Use a Secure File task for Universal Windows Platform app signing</span></span>

<span data-ttu-id="8b8a4-118">セキュリティで保護されたファイル タスクの使用は、Universal Windows Platform (UWP) アプリの署名に推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-118">Using a Secure File task is the recommended approach for Universal Windows Platform (UWP) app signing.</span></span> <span data-ttu-id="8b8a4-119">パッケージ署名の詳細については、[パッケージ署名の構成](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-119">For more information about package signing, see [Configure package signing](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing).</span></span> <span data-ttu-id="8b8a4-120">このプロセスを次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-120">This process is shown in the following image.</span></span>

![MPOS アプリ署名フロー](media/POSSigningFlow.png)

> [!NOTE]
> <span data-ttu-id="8b8a4-122">現在 OOB パッケージでは、appx ファイルの署名のみがサポートされており、MPOIS、RSSU、HWSなどのセルフ サービスの他のインストーラーは、このプロセスによって署名されません。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-122">Currently the OOB packaging supports signing only the appx file, the different self-service installers like MPOIS, RSSU, and HWS are not signed by this process.</span></span> <span data-ttu-id="8b8a4-123">SignTool またはその他の署名ツールを使用して、手動で署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-123">You need to manually sign it using SignTool or other signing tools.</span></span> <span data-ttu-id="8b8a4-124">appx ファイルの署名に使用する証明書は、Modern POS がインストールされているマシンにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-124">The certificate used for signing the appx file must be installed in the machine where Modern POS is installed.</span></span>

## <a name="steps-to-configure-the-certificate-for-signing"></a><span data-ttu-id="8b8a4-125">署名のために証明書を構成する手順</span><span class="sxs-lookup"><span data-stu-id="8b8a4-125">Steps to configure the certificate for signing</span></span>

### <a name="certificate-in-the-file-systemsecure-location"></a><span data-ttu-id="8b8a4-126">ファイル システム / 安全な場所の証明書</span><span class="sxs-lookup"><span data-stu-id="8b8a4-126">Certificate in the file system/secure location</span></span>

<span data-ttu-id="8b8a4-127">[ダウンロードファイル タスク](https://docs.microsoft.com/visualstudio/msbuild/downloadfile-task)をダウンロードして、ビルド プロセスの最初の手順として追加します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-127">Download the [DownloadFile task](https://docs.microsoft.com/visualstudio/msbuild/downloadfile-task) and add it as the first step in the build process.</span></span> <span data-ttu-id="8b8a4-128">セキュリティで保護されたファイルのタスクを使用する利点は、ビルド パイプラインが成功したか、失敗したか、またはキャンセルされたかに関係なく、ビルド時にファイルが暗号化されてディスクに格納されることです。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-128">The advantage of using the Secure File task is that the file is encrypted and placed in the disk during build no matter if the build pipeline succeeds, fails, or is canceled.</span></span> <span data-ttu-id="8b8a4-129">このファイルは、ビルド プロセスの完了後にダウンロード場所から削除されます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-129">The file is deleted from the download location after the build process is completed.</span></span>

1. <span data-ttu-id="8b8a4-130">Azure DevOps ビルド パイプラインの最初のステップとして、セキュア ファイル タスクをダウンロードして追加します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-130">Download and add the Secure File task as the first step in the Azure DevOps build pipeline.</span></span> <span data-ttu-id="8b8a4-131">セキュア ファイル タスクは、[DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-131">You can download the Secure File task from [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).</span></span>
2. <span data-ttu-id="8b8a4-132">次の図に示すように、証明書をセキュア ファイル タスクにアップロードし、出力変数で参照名を設定します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-132">Upload the certificate to the Secure File task and set the Reference name under Output Variables, as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8b8a4-133">![セキュア ファイル タスク](media/SecureFile.png)</span><span class="sxs-lookup"><span data-stu-id="8b8a4-133">![Secure file task](media/SecureFile.png)</span></span>
3. <span data-ttu-id="8b8a4-134">**変数** タブの下の **新しい変数** をクリックして、Azure DevOps パイプラインに新しい変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-134">Create a new variable in the Azure DevOps pipeline by clicking **New Variable** under the **Variables** tab.</span></span>
4. <span data-ttu-id="8b8a4-135">値フィールド **$(MySigningCert.secureFilePath)** に、**CertFile** などの変数の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-135">Provide a name for the variable in the value field **$(MySigningCert.secureFilePath)**, for example, **CertFile**.</span></span>
5. <span data-ttu-id="8b8a4-136">変数を保存します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-136">Save the variable.</span></span>
6. <span data-ttu-id="8b8a4-137">**RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、**ModernPOSPackageCertificateKeyFile** を Azure DevOps パイプラインで作成された変数で更新します (手順 3)。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-137">Open the **Customization.settings** file from **RetailSDK\\BuildTools** and update the **ModernPOSPackageCertificateKeyFile** with the variable name created in the Azure DevOps pipeline (step 3).</span></span> <span data-ttu-id="8b8a4-138">例:</span><span class="sxs-lookup"><span data-stu-id="8b8a4-138">For example:</span></span>

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(CertFile)</ModernPOSPackageCertificateKeyFile>
    ```

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app"></a><span data-ttu-id="8b8a4-139">MPOS アプリに署名するために証明書をダウンロードまたは生成する</span><span class="sxs-lookup"><span data-stu-id="8b8a4-139">Download or generate a certificate to sign the MPOS app</span></span>

<span data-ttu-id="8b8a4-140">ダウンロードまたは生成された証明書を使用して MPOS アプリに署名する場合、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateKeyFile** ノードを更新して、pfx ファイルの場所 (**$(SdkReferencesPath)\\appxsignkey.pfx**) を指すようにします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-140">If a downloaded or generated certificate is used to sign the MPOS app, then the update the **ModernPOSPackageCertificateKeyFile** node in the **BuildTools\\Customization.settings** file to point to the pfx file location (**$(SdkReferencesPath)\\appxsignkey.pfx**).</span></span> <span data-ttu-id="8b8a4-141">例:</span><span class="sxs-lookup"><span data-stu-id="8b8a4-141">For example:</span></span>

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

<span data-ttu-id="8b8a4-142">この場合、証明書ファイル名は **appxsignkey.pfx** であり、**Retail SDK\\ 参照** フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-142">In this case, the certificate file name is **appxsignkey.pfx**, located in the **Retail SDK\\Reference** folder.</span></span>

## <a name="use-thumbprint-to-sign-the-mpos-app"></a><span data-ttu-id="8b8a4-143">拇印を使用して MPOS アプリに署名する</span><span class="sxs-lookup"><span data-stu-id="8b8a4-143">Use thumbprint to sign the MPOS app</span></span>

<span data-ttu-id="8b8a4-144">拇印を使用して MPOS アプリに署名する場合は、証明書をローカルにインストールします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-144">If you use thumbprint to sign the MPOS app, then install the certificate locally.</span></span> <span data-ttu-id="8b8a4-145">**BuildTools\\Customization.settings** ファイルにある **ModernPOSPackageCertificateThumbprint** ノードで、拇印の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-145">Update the thumbprint value in the **ModernPOSPackageCertificateThumbprint** node in the **BuildTools\\Customization.settings** file.</span></span>

<span data-ttu-id="8b8a4-146">このオプションは、ビルド ユーザーがローカル ユーザーの場合に機能します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-146">This option will work if the build user is a local user.</span></span> <span data-ttu-id="8b8a4-147">ただし、Azure DevOps エージェントを使用してビルドを生成している場合、エージェントは証明書ストアにアクセスして署名に証明書を使用する権限を持たないので、ビルド マシンに証明書がインストールされない可能性があります。　</span><span class="sxs-lookup"><span data-stu-id="8b8a4-147">However if you are using the Azure DevOps agents to generate the build, then the agent may not have permission to access the cert store to use the certificate for signing or the build machine will not have the certificate installed.</span></span> <span data-ttu-id="8b8a4-148">この場合、ビルド ユーザーをローカル ユーザーに変更し、そのボックスに証明書をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-148">In this case, the workaround is to change the build user to local user and install the certificate in the box.</span></span> <span data-ttu-id="8b8a4-149">ただし、ボックスへの管理者アクセス権限がない場合は、このオプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-149">However, this option will not work if you don’t have admin access to the box.</span></span>

> [!NOTE]
> <span data-ttu-id="8b8a4-150">pfx file またはセキュア ファイル タスク オプションを使用してアプリに署名する場合は、**Customization.settings** の **ModernPOSPackageCertificateThumbprint** ノードを空のままにします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-150">If the .pfx file or Secure File task option is used to sign the app, then leave the **ModernPOSPackageCertificateThumbprint** node in **Customization.settings** empty.</span></span> <span data-ttu-id="8b8a4-151">拇印オプションが使用されている場合、**ModernPOSPackageCertificateKeyFile** を空のままにします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-151">If the thumbprint option is used, then leave **ModernPOSPackageCertificateKeyFile** empty.</span></span> <span data-ttu-id="8b8a4-152">両方の値を更新すると、ビルドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-152">If both the values are updated, then the build will fail.</span></span>

### <a name="certification-renewal"></a><span data-ttu-id="8b8a4-153">証明書の更新</span><span class="sxs-lookup"><span data-stu-id="8b8a4-153">Certification renewal</span></span>

### <a name="renew-a-certificate-from-trusted-ca"></a><span data-ttu-id="8b8a4-154">信頼される CA から証明書を更新する</span><span class="sxs-lookup"><span data-stu-id="8b8a4-154">Renew a certificate from trusted CA</span></span>

<span data-ttu-id="8b8a4-155">証明書の更新プロセスについては、証明機関 (CA) に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-155">Contact your certifying authority (CA) for the certificate renewal process.</span></span> <span data-ttu-id="8b8a4-156">信頼される証明書については、MPOS 側でアクションを実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-156">For a trusted certificate, no action is required on the MPOS side.</span></span>

### <a name="renew-a-self-signed-certificate"></a><span data-ttu-id="8b8a4-157">自己署名証明書を更新する</span><span class="sxs-lookup"><span data-stu-id="8b8a4-157">Renew a self-signed certificate</span></span>

<span data-ttu-id="8b8a4-158">実稼働用の Retail SDK で使用可能なサンプル証明書は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-158">Don’t use the sample certificate available in the Retail SDK for production.</span></span> <span data-ttu-id="8b8a4-159">開発の目的にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-159">It can be used only for development purposes.</span></span> <span data-ttu-id="8b8a4-160">サンプルの Contoso の証明書は更新することができず、10.0.16 またはそれ以前のバージョンの Retail SDK に含まれているサンプルの証明書は、2020 年 12 月 31 日に有効期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-160">The sample Contoso certificate can't be renewed and the sample certificate included in Retail SDK version 10.0.16 or earlier will expire on December 31, 2020.</span></span> <span data-ttu-id="8b8a4-161">カスタマイズされた Modern POS に署名するためにこの証明書または自己署名証明書を使用した場合、この日付の後は Modern POS が正しく機能しなくなる可能性が大いにあります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-161">If this certificate, or a self-signed certificate, has been used to sign a customized Modern POS, there is a strong possibility that Modern POS will not function properly after this  date.</span></span>
 
### <a name="impact"></a><span data-ttu-id="8b8a4-162">影響</span><span class="sxs-lookup"><span data-stu-id="8b8a4-162">Impact</span></span>
 
<span data-ttu-id="8b8a4-163">上記の場合、2020 年 12 月 31 日以降はインストーラーを実行できないという問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-163">If the above is true for you, the issue you will be encountering is that the installer will not be able to run after December 31, 2020.</span></span> <span data-ttu-id="8b8a4-164">使用している会社の IT ポリシーによっては、Modern POS が機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-164">Depending on the corporate IT policies used, Modern POS may not be able to function.</span></span> <span data-ttu-id="8b8a4-165">組織への影響を判断するために、日付を一時的に未来の日付に変更してテストすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-165">It is critical that you test this by changing the date temporarily to a future date, to determine the impact to your organization.</span></span>
 
### <a name="steps-to-determine-the-issue"></a><span data-ttu-id="8b8a4-166">問題を特定する手順</span><span class="sxs-lookup"><span data-stu-id="8b8a4-166">Steps to determine the issue</span></span>
 
1.  <span data-ttu-id="8b8a4-167">Windows の設定を使用して、コンピュータの日時を 2021 年の時刻に変更します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-167">Use Windows settings to change the computer clock to a date and time in the year 2021.</span></span>
2.  <span data-ttu-id="8b8a4-168">Modern POS を開くことができることを確認し、サインインを実行すると、トランザクションを完了することができます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-168">Verify that Modern POS can be opened, sign in can occur, and a transaction can be completed.</span></span>
3.  <span data-ttu-id="8b8a4-169">Modern POS のセルフ サービス インストーラーが実行可能であることを確認します。実行可能な場合、インストールは正常に完了します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-169">Verify that Modern POS Self-service installer is able to be run, and if so, that installation will complete successfully.</span></span>
4.  <span data-ttu-id="8b8a4-170">Windows の日時設定を正しい時刻に戻します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-170">Return the Windows clock settings to the correct date and time.</span></span>
 
<span data-ttu-id="8b8a4-171">これらの手順すべてを問題なく完了できる場合、現在の証明書で 2020 年 12 月 31 日までの操作が可能になります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-171">If you can complete all of these steps without issues, then you will be able to operate on the current certificate past December 31, 2020.</span></span>  
 
### <a name="steps-going-forward"></a><span data-ttu-id="8b8a4-172">今後の手順</span><span class="sxs-lookup"><span data-stu-id="8b8a4-172">Steps going forward</span></span> 

<span data-ttu-id="8b8a4-173">以前に使用していた証明書を更新することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-173">It is highly recommended that you renew the previously used certificate.</span></span> <span data-ttu-id="8b8a4-174">新しい証明書を取得することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-174">We strongly recommend that you obtain a new certificate.</span></span> <span data-ttu-id="8b8a4-175">これを実行するには、次のアクションのいずれかを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-175">To do this, you must perform one of the following actions:</span></span>
 
- <span data-ttu-id="8b8a4-176">**優先** - 信頼される証明機関からコード署名証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-176">**Preferred** - Obtain a code signing certificate from a trusted certificate authority.</span></span>

- <span data-ttu-id="8b8a4-177">**優先** - 使用する自己署名のコード署名証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-177">**Preferred** - Generate a self-signed code signing certificate to use.</span></span> <span data-ttu-id="8b8a4-178">通常、これはドメイン内で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-178">This is typically used when within a domain.</span></span>

- <span data-ttu-id="8b8a4-179">**一時的なソリューションとして利用可能** - 更新された Contoso のコード署名証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-179">**Available as a temporary Solution** - Use the renewed Contoso code signing certificate.</span></span> <span data-ttu-id="8b8a4-180">通常、これはテスト目的で使用されるため、運用環境に配置することはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-180">This is typically used for testing purposes, so it's not recommended that it be deployed in production.</span></span>
 
<span data-ttu-id="8b8a4-181">次に、上記のいずれかのアクションから取得した証明書を使用して署名された、新しくカスタマイズされた Modern POS のパッケージを生成します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-181">Next, generate a new customized Modern POS package that is signed using this certificate obtained from one of the actions above.</span></span> <span data-ttu-id="8b8a4-182">証明書に応じて、次のいずれかの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-182">Depending on the certificate, one of the following steps must be followed:</span></span>
 
- <span data-ttu-id="8b8a4-183">新しい信頼される証明書 (または新しい自己署名の証明書) を使用する場合、すべてのデバイスに新しい証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-183">If using a new, trusted certificate (or a new, self-signed certificate), you will be  required to install a new certificate on every device.</span></span> <span data-ttu-id="8b8a4-184">その後、新しく作成された Modern POS のパッケージ (インストーラー) を使用して、既存のアプリケーションをアンインストールし、新しい Modern POS パッケージを再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-184">After that, you need to take the newly created Modern POS Package (installer), uninstall the existing application, and then reinstall the new Modern POS package.</span></span> <span data-ttu-id="8b8a4-185">すべてのデバイスで Modern POS のデバイスの有効化を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-185">You will need to perform a device activation of Modern POS on every device.</span></span>

- <span data-ttu-id="8b8a4-186">更新された Contoso 証明書を使用する場合、すべてのデバイスに新しい証明書をインストールして、Modern POS パッケージ (インストーラー) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-186">If using the renewed Contoso certificate, you will be required to install the new certificate on every device and install the Modern POS Package (installer).</span></span> <span data-ttu-id="8b8a4-187">アンインストールする必要はありませんが、デバイスに再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-187">You are not required to uninstall, however you must reinstall on the device.</span></span> <span data-ttu-id="8b8a4-188">Modern POS のデバイスの有効化は必須ではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-188">Note that device activation of Modern POS will not be required.</span></span> <span data-ttu-id="8b8a4-189">このオプションは一時的なソリューションです。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-189">This option is a temporary solution.</span></span> <span data-ttu-id="8b8a4-190">新しい信頼される証明書を取得する前にこのオプションを使用するだけで最有効化を回避し、問題を解決することができます。</span><span class="sxs-lookup"><span data-stu-id="8b8a4-190">Only use this option to avoid reactivation and resolve the issue before obtaining a new trusted certificate.</span></span>
