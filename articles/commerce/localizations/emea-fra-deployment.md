---
title: フランスのキャッシュ レジスターの配置ガイドライン
description: このトピックは、フランスのローカライズ用配置ガイドです。
author: AlexChern0v
manager: ezubov
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: France
ms.search.industry: Retail
ms.author: josaw
ms.search.scope: Retail, Core, Operations
ms.search.validFrom: 2018-4-13
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: d5aa569762671ea649066fde37c4642ed4002926
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973994"
---
# <a name="deployment-guidelines-for-cash-registers-for-france"></a><span data-ttu-id="a0010-103">フランスのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="a0010-103">Deployment guidelines for cash registers for France</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0010-104">このトピックは、Dynamics 365 Commerce のフランスでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="a0010-104">This topic is a deployment guide that shows how to enable the Dynamics 365 Commerce localization for France.</span></span> <span data-ttu-id="a0010-105">ローカライズは、コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="a0010-105">The localization consists of several extensions of components.</span></span> <span data-ttu-id="a0010-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="a0010-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="a0010-107">フランスのローカライズの詳細については、 [フランスのキャッシュ レジスター機能](./emea-fra-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-107">For more information about the localization for France, see [Cash register functionality for France](./emea-fra-cash-registers.md).</span></span>

<span data-ttu-id="a0010-108">このローカライズは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="a0010-108">This localization is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="a0010-109">SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-109">For information about how to install and use the SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="a0010-110">このローカライズは、Commerce runtime (CRT)、Retail Servers、および POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="a0010-110">This localization consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="a0010-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="a0010-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a0010-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="a0010-113">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="a0010-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="a0010-114">Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a0010-114">In Commerce 10.0.8 and above, Retail Server is known as Commerce Scale Unit.</span></span> <span data-ttu-id="a0010-115">このトピックは、アプリの以前の複数のバージョンに適用されるため、このトピック全体で *Retail サーバー*を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0010-115">Because this topic applies to multiple previous versions of the app, *Retail Server* is used throughout the topic.</span></span>

## <a name="storing-a-certificate-for-digital-signing-in-azure-key-vault"></a><span data-ttu-id="a0010-116">Azure Key Vault にデジタル署名用証明書を保存します。</span><span class="sxs-lookup"><span data-stu-id="a0010-116">Storing a certificate for digital signing in Azure Key Vault</span></span>

<span data-ttu-id="a0010-117">デジタル署名拡張機能は、Retail Serverが配置されているマシンのローカルの証明書のストレージにインストールされている証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0010-117">The digital signature extension uses a certificate that is installed in the local certificate storage of the machine where Retail Server is deployed.</span></span> <span data-ttu-id="a0010-118">コンフィギュレーション ファイルの証明書の拇印を指定する必要があります (このトピックで後述する [SequentialSignatureRegisterコンポーネント](#sequentialsignatureregister-component) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="a0010-118">The thumbprint of the certificate must be specified in the configuration file (see the [SequentialSignatureRegister component](#sequentialsignatureregister-component) section later in this topic).</span></span> <span data-ttu-id="a0010-119">実装のトポロジーに応じて、証明書は [Microsoft Azure Key Vault ストレージ](https://docs.microsoft.com/azure/key-vault/key-vault-get-started) に保存される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-119">Depending on the implementation topology, the certificate might have to be stored in [Microsoft Azure Key Vault storage](https://docs.microsoft.com/azure/key-vault/key-vault-get-started).</span></span> <span data-ttu-id="a0010-120">フランス用ローカライズには、Azure Key Vault ストレージに保存されている証明書を使用して、署名フローを上書きし、販売取引に署名する方法を示すサンプル コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a0010-120">The localization for France contains a code sample that shows how to override the signing flow and sign sales transactions by using a certificate that is stored in Azure Key Vault storage.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a0010-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="a0010-121">Prerequisites</span></span>

<span data-ttu-id="a0010-122">Azure Key Vault ストレージに格納されている証明書を使用する前に、次の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-122">The following steps must be completed before you can use a certificate that is stored in Azure Key Vault storage:</span></span>

- <span data-ttu-id="a0010-123">Azure Key Vault ストレージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-123">The Azure Key Vault storage must be created.</span></span> <span data-ttu-id="a0010-124">Retail Server と同じ地理的領域にストレージを配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a0010-124">We recommend that you deploy the storage in the same geographical region as the Retail Server.</span></span>
- <span data-ttu-id="a0010-125">証明書は、そのストレージにアップロードされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-125">The certificate must be uploaded to the storage.</span></span>
- <span data-ttu-id="a0010-126">ストレージから機密情報を読み取るには、Retail Server アプリケーションが承認される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-126">The Retail Server application must be authorized to read secrets from the storage.</span></span>

<span data-ttu-id="a0010-127">Azure Key Vault を操作する方法の詳細については、次を参照してください。[Azure Key Vault の使用を開始します](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)。</span><span class="sxs-lookup"><span data-stu-id="a0010-127">For more information about how to work with Azure Key Vault, see [Get started with Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-get-started).</span></span>

### <a name="using-the-sample"></a><span data-ttu-id="a0010-128">サンプルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-128">Using the sample</span></span>

<span data-ttu-id="a0010-129">**DigitalSignatureKeyVaultSample** プロジェクトは、Azure Key Vault ストレージに格納されている証明書を使用するためのサンプル コードを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="a0010-129">The **DigitalSignatureKeyVaultSample** project contains sample code that uses a certificate that is stored in Azure Key Vault storage.</span></span> <span data-ttu-id="a0010-130">サンプルを実稼働環境で使用するには、ロジックを実装し、**CertificateSignatureServiceRequestHandler** クラスにある **HashAndSignData** メソッドで、次のパラメータを指定できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-130">To use the sample in a production environment, you must implement logic so that the following parameters can be specified in the **HashAndSignData** method of the **CertificateSignatureServiceRequestHandler** class:</span></span>

- <span data-ttu-id="a0010-131">**Azure Key Vault URL** - Azure Key Vault ストレージの URL。</span><span class="sxs-lookup"><span data-stu-id="a0010-131">**Azure Key Vault URL** – The URL of the Azure Key Vault storage.</span></span>

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultUrl, "Set your Azure Key Vault URL here");
    ```

- <span data-ttu-id="a0010-132">**クライアント ID** - 認証のために Azure Key Vault ストレージに関連付けられている Azure Active Directory (Azure AD) アプリケーションのインタラクティブ クライアント ID。</span><span class="sxs-lookup"><span data-stu-id="a0010-132">**Client ID** – An interactive client ID of the Azure Active Directory (Azure AD) application that is associated with the Azure Key Vault storage for authentication purposes.</span></span> <span data-ttu-id="a0010-133">このクライアントは、 Azure Key Vault ストレージから機密情報を読み取るためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="a0010-133">This client should have access to read secrets from the Azure Key Vault storage.</span></span>

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultInteractiveClientId, "Set the client ID here");
    ```

- <span data-ttu-id="a0010-134">**クライアント シークレット** - Azure Key Vault ストレージで認証のために使用される Azure AD アプリケーションと関連している秘密キー。</span><span class="sxs-lookup"><span data-stu-id="a0010-134">**Client secret** – A secret key that is associated with the Azure AD application that is used for authentication in the Azure Key Vault storage.</span></span>

    ``` csharp
    // Secret key value should be encrypted and stored in a safe place.
    settings.Add(WellKnownKeyVaultSettings.KeyVaultClientSecretKey, "Set the secret key here");
    ```

- <span data-ttu-id="a0010-135">**秘密参照**- 証明書への秘密の参照。</span><span class="sxs-lookup"><span data-stu-id="a0010-135">**Secret reference** – A secret reference to the certificate.</span></span>

    ``` csharp
    SecretCertificate secretCertificate = settingsHelper.SecretProvider.GetSecret("vault:///{Specify the secret reference}") as SecretCertificate;
    ```

<span data-ttu-id="a0010-136">署名のフローを上書きする場合は以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0010-136">To override the signing flow, follow these steps.</span></span>

1. <span data-ttu-id="a0010-137">**DigitalSignatureKeyVaultSample** プロジェクトを構築し、、**Contoso.Commerce.Runtime.DigitalSignatureKeyVaultSample.dll** アセンブリを **bin\\ext** Retail Server folder にコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-137">Build the **DigitalSignatureKeyVaultSample** project, and copy the **Contoso.Commerce.Runtime.DigitalSignatureKeyVaultSample.dll** assembly to the **bin\\ext** Retail Server folder.</span></span>
2. <span data-ttu-id="a0010-138">**コンポジション** セクションに次の行を追加して、**commerceRuntime.ext.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="a0010-138">Update the **commerceRuntime.ext.config** file by adding the following line to the **composition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
    ```

> [!NOTE]
> <span data-ttu-id="a0010-139">デジタル署名に使用される証明書の拇印は、証明書が Azure Key Vault ストレージに保存されている場合でも、SequentialSignatureRegister アセンブリのコンフィギュレーション ファイルで指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-139">The thumbprint of the certificate that is used for digital signing should be specified in the configuration file of the SequentialSignatureRegister assembly, even if the certificate is stored in Azure Key Vault storage.</span></span> <span data-ttu-id="a0010-140">詳細については、このトピックの後半の [SequentialSignatureRegister コンポーネント](#sequentialsignatureregister-component) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-140">For more information, see the [SequentialSignatureRegister component](#sequentialsignatureregister-component) section later in this topic.</span></span>

### <a name="using-certificate-profiles-in-commerce-channels"></a><span data-ttu-id="a0010-141">Commerce チャネルでの証明書プロファイルの使用</span><span class="sxs-lookup"><span data-stu-id="a0010-141">Using certificate profiles in Commerce channels</span></span>

<span data-ttu-id="a0010-142">Commerce バージョン 10.0.15では、Key Vaultまたは本社が使用できない場合に、オフラインにするためのフェールオーバーをサポートする[小売店舗のユーザー定義の証明書プロファイル](./certificate-profiles-for-retail-stores.md) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0010-142">In Commerce version 10.0.15 and later, you can use the [User-defined certificate profiles for retail stores](./certificate-profiles-for-retail-stores.md) feature that supports failover to offline when Key Vault or Headquarters are not available.</span></span> <span data-ttu-id="a0010-143">この機能は、[小売チャンネルのシークレットを管理 ](../dev-itpro/manage-secrets.md) を拡張ます。</span><span class="sxs-lookup"><span data-stu-id="a0010-143">The feature extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature.</span></span>

<span data-ttu-id="a0010-144">CRT の新しい機能を適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0010-144">To apply the new feature in the CRT extension, follow these steps.</span></span>

1. <span data-ttu-id="a0010-145">新しい CRT 拡張機能プロジェクトを作成します (C# クラス ライブラリ プロジェクト タイプ)。</span><span class="sxs-lookup"><span data-stu-id="a0010-145">Create a new CRT extension project (C# class library project type).</span></span> <span data-ttu-id="a0010-146">Retail ソフトウェア開発キット (SDK) からサンプル テンプレートを使用します (RetailSDK\SampleExtensions\CommerceRuntime)。</span><span class="sxs-lookup"><span data-stu-id="a0010-146">Use the sample templates from the Retail software development kit (SDK) (RetailSDK\SampleExtensions\CommerceRuntime).</span></span>

2. <span data-ttu-id="a0010-147">CertificateSignatureServiceRequest のカスタム ハンドラーを SequentialSignatureRegister プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="a0010-147">Add custom handler for CertificateSignatureServiceRequest in the SequentialSignatureRegister project.</span></span>

3. <span data-ttu-id="a0010-148">シークレット呼び出しを読み取るには、プロファイスされたパラメータのあるコンストラクターを使用し、GetUserDefinedSecretCertificateServiceRequest を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0010-148">To read a secret call, GetUserDefinedSecretCertificateServiceRequest using a constructor with profileId parameter.</span></span> <span data-ttu-id="a0010-149">これにより、証明書プロファイルの設定で機能が開始されます。</span><span class="sxs-lookup"><span data-stu-id="a0010-149">That will start the functionality working with settings from Certificate profiles.</span></span> <span data-ttu-id="a0010-150">この設定に基づいて、証明書は Azure Key Vault またはローカルマシン ストレージから取得されます。</span><span class="sxs-lookup"><span data-stu-id="a0010-150">Based on the settings, the certificate will be retrieved either from Azure Key Vault or local machine storage.</span></span>
    
    <span data-ttu-id="a0010-151">GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);  GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);</span><span class="sxs-lookup"><span data-stu-id="a0010-151">GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);  GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);</span></span>
    
    <span data-ttu-id="a0010-152">X509Certificate2 証明書 = getUserDefinedSecretCertificateServiceResponse.Certificate;</span><span class="sxs-lookup"><span data-stu-id="a0010-152">X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;</span></span>
    
4. <span data-ttu-id="a0010-153">証明書が取得されたら、データ署名に進みます。</span><span class="sxs-lookup"><span data-stu-id="a0010-153">When the certificate is retrieved, proceed with data signing.</span></span>

5. <span data-ttu-id="a0010-154">CRT 拡張機能プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0010-154">Build the CRT extension project.</span></span>

6. <span data-ttu-id="a0010-155">出力クラス ライブラリをコピーし、手動テスト用の ...\RetailServer\webroot\bin\Ext に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="a0010-155">Copy the output class library and paste it into ...\RetailServer\webroot\bin\Ext for manual testing.</span></span>

7. <span data-ttu-id="a0010-156">CommerceRuntime.Ext.config ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="a0010-156">In the CommerceRuntime.Ext.config file, update the extension composition section with the custom library information.</span></span>

## <a name="specifying-application-attributes-that-will-be-printed-on-receipts"></a><span data-ttu-id="a0010-157">レシートに印刷されるアプリケーション属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0010-157">Specifying application attributes that will be printed on receipts</span></span>

<span data-ttu-id="a0010-158">カスタム フィールドを使用することで、次のようなアプリケーション属性をレシートに印刷できます。</span><span class="sxs-lookup"><span data-stu-id="a0010-158">You can use custom fields to print the following application attributes on receipts</span></span><!-- (for more information, see [Cash registers for France](./emea-fra-cash-registers.md))--><span data-ttu-id="a0010-159">:</span><span class="sxs-lookup"><span data-stu-id="a0010-159">:</span></span>

- <span data-ttu-id="a0010-160">**ビルド番号**- POS アプリケーションのソフトウェアのバージョン。</span><span class="sxs-lookup"><span data-stu-id="a0010-160">**Build number** – The software version of the POS application.</span></span> <span data-ttu-id="a0010-161">既定では、この値は、Microsoft が POS アプリケーションに割り当てた POS ビルド番号と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="a0010-161">By default, the value should equal the POS build number that Microsoft assigned to the POS application.</span></span>
- <span data-ttu-id="a0010-162">**証明書のカテゴリ**および**証明書の番号** - アプリケーションの認定証明を発行するカテゴリとコンプライアンスの証明書の数。</span><span class="sxs-lookup"><span data-stu-id="a0010-162">**Certificate category** and **Certificate number** – The category and number of the certificate of compliance that an accredited body issues for the application.</span></span> <span data-ttu-id="a0010-163">既定では、値はカテゴリとMicrosoft に与えられた証明書の数に等しい。</span><span class="sxs-lookup"><span data-stu-id="a0010-163">By default, the values equal the category and the number of the certificate that is granted to Microsoft:</span></span>

    - <span data-ttu-id="a0010-164">Microsoft Dynamics 365 for Commerce:</span><span class="sxs-lookup"><span data-stu-id="a0010-164">Microsoft Dynamics 365 for Commerce:</span></span>

        - <span data-ttu-id="a0010-165">**証明書のカテゴリ:** C</span><span class="sxs-lookup"><span data-stu-id="a0010-165">**Certificate category:** C</span></span>
        - <span data-ttu-id="a0010-166">**証明書番号:** 18/0202</span><span class="sxs-lookup"><span data-stu-id="a0010-166">**Certificate number:** 18/0202</span></span>

    - <span data-ttu-id="a0010-167">Microsoft Dynamics 365 for Commerce:</span><span class="sxs-lookup"><span data-stu-id="a0010-167">Microsoft Dynamics 365 for Commerce:</span></span>

        - <span data-ttu-id="a0010-168">**証明書のカテゴリ:** B</span><span class="sxs-lookup"><span data-stu-id="a0010-168">**Certificate category:** B</span></span>
        - <span data-ttu-id="a0010-169">**証明書番号:** 18/0203</span><span class="sxs-lookup"><span data-stu-id="a0010-169">**Certificate number:** 18/0203</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0010-170">既定では、証明書のカテゴリおよび割り当てられている番号が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="a0010-170">By default, the certificate category and number that are assigned are printed.</span></span> <span data-ttu-id="a0010-171">コマースを実装している場合は、証明書のカテゴリと番号を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-171">If you're implementing Commerce, you must override the certificate category and number.</span></span>

<span data-ttu-id="a0010-172">POS アプリケーションをカスタマイズしていて、そのカスタマイズがアプリケーションのコンプライアンスに影響を与える場合は、認定機関にコンプライアンスの新しい証明書を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-172">If you customize the POS application, and your customizations affect the compliance of the application, you might have to request a new certificate of compliance from an accredited body.</span></span> <span data-ttu-id="a0010-173">この場合、ビルド番号、および証明書のカテゴリ、および番号を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-173">In this case, you must override the build number, and the certificate category and number.</span></span> <span data-ttu-id="a0010-174">それ以外の場合、証明書のカテゴリおよび番号の既定値が印刷されますが、Microsoft が POS アプリケーションに割り当てた POS ビルド番号も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-174">Otherwise, the default values for the certificate category and number will be printed, but you must still specify the POS build number that Microsoft assigned to the POS application.</span></span>

### <a name="overriding-the-build-number"></a><span data-ttu-id="a0010-175">ビルド番号の変更</span><span class="sxs-lookup"><span data-stu-id="a0010-175">Overriding the build number</span></span>

<span data-ttu-id="a0010-176">ソフトウェアのバージョン/ビルド番号と発行元は、**RetailSDK\\BuildTools\\Customization.settings** で指定されます。</span><span class="sxs-lookup"><span data-stu-id="a0010-176">The software version/build number and publisher are specified in **RetailSDK\\BuildTools\\Customization.settings**.</span></span>

```xml
<CustomVersion Condition="'$(CustomVersion)' == ''">1.0.0.1</CustomVersion>
<CustomName Condition="'$(CustomName)' == ''">Contoso Retail Customization</CustomName> 
<CustomDescription Condition="'$(CustomDescription)' == ''">Contoso Retail Customization</CustomDescription>
<CustomPublisher Condition="'$(CustomPublisher)' == ''">CN=Contoso Ltd.</CustomPublisher>
<CustomPublisherDisplayName Condition="'$(CustomPublisherDisplayName)' == ''">Contoso Ltd.</CustomPublisherDisplayName>
<CustomCopyright Condition="'$(CustomCopyright)' == ''">Copyright © 2016</CustomCopyright>
```

### <a name="overriding-the-certificate-category-and-number"></a><span data-ttu-id="a0010-177">証明書のカテゴリや番号の変更</span><span class="sxs-lookup"><span data-stu-id="a0010-177">Overriding the certificate category and number</span></span>

<span data-ttu-id="a0010-178">証明書のカテゴリと番号は、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsFrance\\GetSalesTransactionCustomReceiptFieldService** で指定されます。</span><span class="sxs-lookup"><span data-stu-id="a0010-178">The certificate category and number are specified in **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsFrance\\GetSalesTransactionCustomReceiptFieldService**.</span></span>

``` csharp
/// <summary>
/// Certification category.
/// </summary>
private const string CertificationCategory = "C";

/// <summary>
/// Certificate number.
/// </summary>
private const string CertificateNumber = "18/0202";
```

> [!NOTE]
> <span data-ttu-id="a0010-179">コマースを実装している場合は、証明書のカテゴリと番号も上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-179">You must also override the certificate category and number if you're implementing Commerce.</span></span> <span data-ttu-id="a0010-180">この場合、このトピックで先に見たセクション、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) にある証明書のカテゴリおよびに記載されている証明書のカテゴリと番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0010-180">In this case, use the certificate category and number that are provided in the [Specifying application attributes that will be printed on receipts](#specifying-application-attributes-that-will-be-printed-on-receipts) section earlier in this topic.</span></span>

## <a name="development-environment"></a><span data-ttu-id="a0010-181">開発環境</span><span class="sxs-lookup"><span data-stu-id="a0010-181">Development environment</span></span>

<span data-ttu-id="a0010-182">次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a0010-182">Follow these steps to set up a development environment so that you can test and extend the localization functionality.</span></span>

### <a name="crt-extension-components"></a><span data-ttu-id="a0010-183">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-183">CRT extension components</span></span>

<span data-ttu-id="a0010-184">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0010-184">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="a0010-185">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="a0010-185">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="commonfrance-component"></a><span data-ttu-id="a0010-186">CommonFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-186">CommonFrance component</span></span>

1. <span data-ttu-id="a0010-187">**Runtime.Extensions.CommonFrance** プロジェクトを見つけ、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-187">Find the **Runtime.Extensions.CommonFrance** project, and build it.</span></span>
2. <span data-ttu-id="a0010-188">**Extensions.CommonFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.CommonFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-188">In the **Extensions.CommonFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.CommonFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-189">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-189">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-190">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-190">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-191">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-191">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="a0010-192">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-192">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-193">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-193">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-194">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-194">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="a0010-195">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-195">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
    ```

#### <a name="receiptsfrance-component"></a><span data-ttu-id="a0010-196">ReceiptsFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-196">ReceiptsFrance component</span></span>

1. <span data-ttu-id="a0010-197">**Runtime.Extensions.ReceiptsFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-197">Find the **Runtime.Extensions.ReceiptsFrance** project, and build it.</span></span>
2. <span data-ttu-id="a0010-198">**Extensions.ReceiptsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-198">In the **Extensions.ReceiptsFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-199">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-199">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-200">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-200">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-201">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-201">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="a0010-202">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-202">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-203">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-203">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-204">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-204">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="a0010-205">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-205">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
    ```

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="a0010-206">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-206">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="a0010-207">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-207">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="a0010-208">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-208">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-209">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-209">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-210">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-210">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-211">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-211">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="a0010-212">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-212">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-213">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-213">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-214">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-214">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="a0010-215">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-215">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

#### <a name="salespaymenttransextfrance-component"></a><span data-ttu-id="a0010-216">SalesPaymentTransExtFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-216">SalesPaymentTransExtFrance component</span></span>

1. <span data-ttu-id="a0010-217">**Runtime.Extensions.SalesPaymentTransExtFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-217">Find the **Runtime.Extensions.SalesPaymentTransExtFrance** project, and build it.</span></span>
2. <span data-ttu-id="a0010-218">**Extensions.SalesPaymentTransExtFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-218">In the **Extensions.SalesPaymentTransExtFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-219">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-219">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-220">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-220">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-221">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-221">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="a0010-222">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-222">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-223">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-223">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-224">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-224">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="a0010-225">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-225">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
    ```

#### <a name="sequentialsignaturefrance-component"></a><span data-ttu-id="a0010-226">SequentialSignatureFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-226">SequentialSignatureFrance component</span></span>

1. <span data-ttu-id="a0010-227">**Runtime.Extensions.SequentialSignatureFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-227">Find the **Runtime.Extensions.SequentialSignatureFrance** project, and build it.</span></span>
2. <span data-ttu-id="a0010-228">**Extensions.SequentialSignatureFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-228">In the **Extensions.SequentialSignatureFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-229">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-229">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-230">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-230">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-231">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-231">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="a0010-232">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-232">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-233">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-233">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-234">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-234">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="a0010-235">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-235">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
    ```

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="a0010-236">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-236">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="a0010-237">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-237">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="a0010-238">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="a0010-238">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="a0010-239">**CertificateThumbprint** プロパティは、唯一の必須のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="a0010-239">The **certificateThumbprint** property is the only mandatory property.</span></span> <span data-ttu-id="a0010-240">この値は必ず文字列で、40 字の長さがあり、大文字で、区切り記号を含みません。</span><span class="sxs-lookup"><span data-stu-id="a0010-240">The value must be a string that is 40 characters long in upper case and that doesn't include any delimiters.</span></span> <span data-ttu-id="a0010-241">詳細については、[証明書の拇印を取得する方法](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-241">For more information, see [How to retrieve the thumbprint of a certificate](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate).</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <configuration>
        <configSections>
            <section name="SequentialSignatureRegister" type="Contoso.Commerce.Runtime.SequentialSignatureRegister.Configuration.SequentialSignatureRegisterConfigSection, Contoso.Commerce.Runtime.SequentialSignatureRegister"/>
        </configSections>
        <SequentialSignatureRegister certificateThumbprint="insert key certificateThumbprint here" certificateStoreLocation="LocalMachine" certificateStoreName="My"/>
        <startup>
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5.1"/>
        </startup>
    </configuration>
    ```

3. <span data-ttu-id="a0010-242">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-242">Build the project.</span></span>
4. <span data-ttu-id="a0010-243">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-243">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="a0010-244">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="a0010-244">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="a0010-245">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="a0010-245">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="a0010-246">ファイルを CRT 拡張フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-246">Copy the files to the CRT extension folder:</span></span>

    - <span data-ttu-id="a0010-247">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-247">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-248">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-248">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="a0010-249">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-249">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-250">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-250">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-251">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-251">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="a0010-252">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-252">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="a0010-253">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-253">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="a0010-254">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-254">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project, and build it.</span></span>
2. <span data-ttu-id="a0010-255">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-255">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-256">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-256">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-257">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-257">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-258">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-258">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="xzreportsfrance-component"></a><span data-ttu-id="a0010-259">XZReportsFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-259">XZReportsFrance component</span></span>

1. <span data-ttu-id="a0010-260">**Runtime.Extensions.XZReportsFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-260">Find the **Runtime.Extensions.XZReportsFrance** project, and build it.</span></span>
2. <span data-ttu-id="a0010-261">**Extensions.XZReportsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-261">In the **Extensions.XZReportsFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-262">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-262">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-263">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-263">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-264">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-264">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="a0010-265">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-265">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-266">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-266">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-267">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-267">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="a0010-268">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-268">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
    ```

#### <a name="restrictingshiftduration-component"></a><span data-ttu-id="a0010-269">RestrictingShiftDuration コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-269">RestrictingShiftDuration component</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-270">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-270">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

1. <span data-ttu-id="a0010-271">**Runtime.Extensions.RestrictingShiftDuration** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-271">Find the **Runtime.Extensions.RestrictingShiftDuration** project, and build it.</span></span>
2. <span data-ttu-id="a0010-272">**Extensions.RestrictingShiftDuration\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RestrictingShiftDuration.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-272">In the **Extensions.RestrictingShiftDuration\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RestrictingShiftDuration.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-273">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-273">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="a0010-274">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-274">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-275">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-275">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="a0010-276">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-276">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-277">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-277">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-278">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-278">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="a0010-279">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-279">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RestrictingShiftDuration" />
    ```

# <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-280">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-280">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

1. <span data-ttu-id="a0010-281">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-281">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-282">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-282">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-283">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-283">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="a0010-284">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-284">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    ```

# <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-285">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-285">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

1. <span data-ttu-id="a0010-286">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-286">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="a0010-287">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-287">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="a0010-288">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-288">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="a0010-289">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-289">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    ```

---

### <a name="retail-server-extension-components"></a><span data-ttu-id="a0010-290">Retail Server 拡張機能コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-290">Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="a0010-291">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-291">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="a0010-292">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-292">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="a0010-293">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-293">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="a0010-294">IIS Retail Server サイトの場所の **\\bin\\ext** フォルダーにアセンブリ ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-294">Copy the assembly file to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
4. <span data-ttu-id="a0010-295">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-295">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="a0010-296">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-296">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>
5. <span data-ttu-id="a0010-297">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-297">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

### <a name="proxy-extension-component"></a><span data-ttu-id="a0010-298">プロキシ拡張機能コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-298">Proxy extension component</span></span>

<span data-ttu-id="a0010-299">Modern POS に対してオフライン モードで拡張機能を有効にする次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-299">You must complete the following procedure to enable the extensions in offline mode for Modern POS.</span></span>

#### <a name="salestransactionsignature-retail-proxy-sample-component"></a><span data-ttu-id="a0010-300">SalesTransactionSignature Retail プロキシ サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-300">SalesTransactionSignature Retail proxy sample component</span></span>

1. <span data-ttu-id="a0010-301">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="a0010-301">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="a0010-302">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0010-302">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>
3. <span data-ttu-id="a0010-303">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-303">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="a0010-304">拡張機能コンフィギュレーション ファイルで、プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="a0010-304">Register the proxy change in the extensions configuration file.</span></span> <span data-ttu-id="a0010-305">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-305">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

### <a name="modern-pos-extension-components"></a><span data-ttu-id="a0010-306">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-306">Modern POS extension components</span></span>

1. <span data-ttu-id="a0010-307">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0010-307">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="a0010-308">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0010-308">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0010-309">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="a0010-309">Modern POS must not be customized.</span></span> <span data-ttu-id="a0010-310">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-310">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="a0010-311">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="a0010-311">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-312">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-312">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="a0010-313">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-313">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-314">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-314">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-315">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-315">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-316">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="a0010-316">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="a0010-317">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-317">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-318">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-318">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="a0010-319">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-319">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-320">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-320">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-321">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-321">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-322">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-322">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-323">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-323">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="a0010-324">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-324">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-325">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-325">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-326">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-326">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-327">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-327">SalesTransBuildNumberSample</span></span>

    ---

    > [!NOTE]
    > <span data-ttu-id="a0010-328">プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで**すべてのファイルを表示する** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0010-328">To view all files in the project folder, not just the files that are included in the project, select the **Show All Files** button in Solution Explorer.</span></span> <span data-ttu-id="a0010-329">このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-329">If this button isn't available, make sure that you selected the project.</span></span> <span data-ttu-id="a0010-330">現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-330">The icons of files and folders that aren't currently part of the project have a dotted outline.</span></span> <span data-ttu-id="a0010-331">プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0010-331">Right-click the folder to include in the project, and then select **Include in Project**.</span></span>

3. <span data-ttu-id="a0010-332">**tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a0010-332">Enable the extensions to be compiled by removing the following folders from the exclude list in **tsconfig.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-333">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-333">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="a0010-334">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-334">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-335">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-335">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-336">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-336">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-337">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="a0010-337">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="a0010-338">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-338">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-339">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-339">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="a0010-340">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-340">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-341">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-341">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-342">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-342">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-343">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-343">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-344">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-344">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="a0010-345">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-345">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-346">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-346">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-347">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-347">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-348">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-348">SalesTransBuildNumberSample</span></span>

    ---

4. <span data-ttu-id="a0010-349">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="a0010-349">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-350">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-350">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "RestrictingShiftDuration"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-351">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-351">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-352">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-352">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    ---

    > [!NOTE]
    > <span data-ttu-id="a0010-353">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-353">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="a0010-354">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="a0010-354">Rebuild the solution.</span></span>
6. <span data-ttu-id="a0010-355">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="a0010-355">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="a0010-356">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a0010-356">Cloud POS extension components</span></span>

1. <span data-ttu-id="a0010-357">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0010-357">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="a0010-358">**Pos.Extensions** プロジェクトで、既存のソース コードのフォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="a0010-358">Include the following existing source code folders in the **Pos.Extensions** project:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-359">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-359">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="a0010-360">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-360">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-361">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-361">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-362">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-362">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-363">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="a0010-363">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="a0010-364">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-364">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-365">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-365">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="a0010-366">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-366">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-367">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-367">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-368">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-368">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-369">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-369">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-370">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-370">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="a0010-371">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-371">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-372">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-372">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-373">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-373">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-374">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-374">SalesTransBuildNumberSample</span></span>

    ---

    > [!NOTE]
    > <span data-ttu-id="a0010-375">プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで**すべてのファイルを表示する** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0010-375">To view all files in the project folder, not just the files that are included in the project, select the **Show All Files** button in Solution Explorer.</span></span> <span data-ttu-id="a0010-376">このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-376">If this button isn't available, make sure that you selected the project.</span></span> <span data-ttu-id="a0010-377">現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-377">The icons of files and folders that aren't currently part of the project have a dotted outline.</span></span> <span data-ttu-id="a0010-378">プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0010-378">Right-click the folder to include in the project, and then select **Include in Project**.</span></span>

3. <span data-ttu-id="a0010-379">**tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a0010-379">Enable the extensions to be compiled by removing the following folders from the exclude list in **tsconfig.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-380">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-380">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="a0010-381">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-381">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-382">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-382">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-383">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-383">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-384">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="a0010-384">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="a0010-385">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-385">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-386">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-386">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="a0010-387">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-387">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-388">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-388">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-389">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-389">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-390">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-390">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-391">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-391">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="a0010-392">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-392">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="a0010-393">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="a0010-393">SequentialSignature</span></span>
    - <span data-ttu-id="a0010-394">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="a0010-394">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="a0010-395">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="a0010-395">SalesTransBuildNumberSample</span></span>

    ---

4. <span data-ttu-id="a0010-396">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="a0010-396">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-397">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-397">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "RestrictingShiftDuration"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-398">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-398">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-399">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-399">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/RestrictShiftDuration"
    },
    {
        "baseUrl": "Microsoft/AuditEvent.FR"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SequentialSignature"
    },
    {
        "baseUrl": "AuditEventSignatureSample"
    },
    {
        "baseUrl": "SalesTransBuildNumberSample"
    }
    ```

    ---

    > [!NOTE]
    > <span data-ttu-id="a0010-400">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-400">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="a0010-401">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="a0010-401">Rebuild the solution.</span></span>
6. <span data-ttu-id="a0010-402">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0010-402">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="a0010-403">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="a0010-403">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="a0010-404">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="a0010-404">Set up required parameters in Headquarters</span></span>

<span data-ttu-id="a0010-405">詳細については、 [フランスのキャッシュ レジスター機能](./emea-fra-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-405">For more information, see [Cash register functionality for France](./emea-fra-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="a0010-406">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="a0010-406">Production environment</span></span>

<span data-ttu-id="a0010-407">以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="a0010-407">Follow these steps to create deployable packages that contain Commerce components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="a0010-408">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="a0010-408">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="a0010-409">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="a0010-409">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="a0010-410">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="a0010-410">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-411">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-411">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RestrictingShiftDuration" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-412">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-412">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
        <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-413">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-413">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
        <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
        ```

        ---

        <span data-ttu-id="a0010-414">デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="a0010-414">To use a certificate that is stored in Azure Key Vault storage for digital signing, add the following line.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a0010-415">この明細行を追加する前に、このトピックの前の方にある[Azure Key Vault にデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-415">Before you add this line, complete the steps in the [Storing a certificate for digital signing in Azure Key Vault](#storing-a-certificate-for-digital-signing-in-azure-key-vault) section earlier in this topic.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
        ```

    2. <span data-ttu-id="a0010-416">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに以下の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="a0010-416">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

3. <span data-ttu-id="a0010-417">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="a0010-417">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="a0010-418">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージにコマース プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="a0010-418">Add the following lines to the **ItemGroup** section to include the Commerce proxy extension in the deployable packages.</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

    2. <span data-ttu-id="a0010-419">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="a0010-419">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="a0010-420">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-420">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.CommonFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RestrictingShiftDuration.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsFrance.dll" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="a0010-421">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-421">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.CommonFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsFrance.dll" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="a0010-422">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0010-422">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.CommonFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureFrance.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsFrance.dll" />
        ```

        ---

        <span data-ttu-id="a0010-423">デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="a0010-423">To use a certificate that is stored in Azure Key Vault storage for digital signing, add the following line.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a0010-424">この明細行を追加する前に、このトピックの前の方にある、[Azure Key Vaultにデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) セクションにある手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-424">Before you add this line, complete the steps in the [Storing a certificate for digital signing in Azure Key Vault](#storing-a-certificate-for-digital-signing-in-azure-key-vault) section, earlier in this topic.</span></span>

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DataSignatureKeyVaultSample.dll" />
        ```

    3. <span data-ttu-id="a0010-425">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="a0010-425">Add the following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages.</span></span>

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

4. <span data-ttu-id="a0010-426">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="a0010-426">Update the Retail Server configuration file.</span></span> <span data-ttu-id="a0010-427">**RetailSDK\\Packages\\RetailServer\\Code\\ web.config**で、**extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="a0010-427">In **RetailSDK\\Packages\\RetailServer\\Code\\web.config**, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

5. <span data-ttu-id="a0010-428">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="a0010-428">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="a0010-429">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0010-429">Then copy the configuration file to the **References** folder.</span></span> <span data-ttu-id="a0010-430">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="a0010-430">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>
6. <span data-ttu-id="a0010-431">ビルド番号、カテゴリ、および必要に応じて、コンプライアンスの証明書の番号を上書きします。</span><span class="sxs-lookup"><span data-stu-id="a0010-431">Override the build number and the category and number of the certificate of compliance, as required.</span></span> <span data-ttu-id="a0010-432">詳細については、このトピックの前の方にある、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) セクションにある指示を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-432">For more information, see the instructions in the [Specifying application attributes that will be printed on receipts](#specifying-application-attributes-that-will-be-printed-on-receipts) section earlier in this topic.</span></span>
7. <span data-ttu-id="a0010-433">Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0010-433">Start the MSBuild Command Prompt for Visual Studio utility, and run **msbuild** under the Retail SDK folder to create deployable packages.</span></span>
8. <span data-ttu-id="a0010-434">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="a0010-434">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="a0010-435">詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0010-435">For more information, see [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="a0010-436">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a0010-436">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="a0010-437">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0010-437">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="a0010-438">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a0010-438">Sign in to POS.</span></span>
2. <span data-ttu-id="a0010-439">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0010-439">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="a0010-440">**ダウンロードの保留中**フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="a0010-440">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="a0010-441">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="a0010-441">Sign out of POS.</span></span>
4. <span data-ttu-id="a0010-442">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="a0010-442">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="a0010-443">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a0010-443">Sign in to POS.</span></span>
6. <span data-ttu-id="a0010-444">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0010-444">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="a0010-445">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="a0010-445">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="a0010-446">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="a0010-446">Restart Modern POS.</span></span>
