---
title: フランスのキャッシュ レジスターの配置ガイドライン
description: このトピックは、フランスのローカライズ用配置ガイドです。
author: AlexChern0v
manager: ezubov
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.search.region: France
ms.search.industry: Retail
ms.author: v-alexec
ms.search.validFrom: 2018-4-13
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 95b6fa493dc211424f734b92833a32ba06e71cdd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057576"
---
# <a name="deployment-guidelines-for-cash-registers-for-france"></a><span data-ttu-id="cffa1-103">フランスのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="cffa1-103">Deployment guidelines for cash registers for France</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cffa1-104">このトピックは、Dynamics 365 Commerce のフランスでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="cffa1-104">This topic is a deployment guide that shows how to enable the Dynamics 365 Commerce localization for France.</span></span> <span data-ttu-id="cffa1-105">ローカライズは、コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-105">The localization consists of several extensions of components.</span></span> <span data-ttu-id="cffa1-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="cffa1-107">フランスのローカライズの詳細については、 [フランスのキャッシュ レジスター機能](./emea-fra-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-107">For more information about the localization for France, see [Cash register functionality for France](./emea-fra-cash-registers.md).</span></span>

<span data-ttu-id="cffa1-108">このローカライズは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="cffa1-108">This localization is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="cffa1-109">SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-109">For information about how to install and use the SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="cffa1-110">このローカライズは、Commerce runtime (CRT)、Retail Servers、および POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-110">This localization consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="cffa1-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="cffa1-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="cffa1-113">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="cffa1-114">Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-114">In Commerce 10.0.8 and above, Retail Server is known as Commerce Scale Unit.</span></span> <span data-ttu-id="cffa1-115">このトピックは、アプリの以前の複数のバージョンに適用されるため、このトピック全体で *Retail サーバー*を使用します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-115">Because this topic applies to multiple previous versions of the app, *Retail Server* is used throughout the topic.</span></span>

## <a name="storing-a-certificate-for-digital-signing-in-azure-key-vault"></a><span data-ttu-id="cffa1-116">Azure Key Vault にデジタル署名用証明書を保存します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-116">Storing a certificate for digital signing in Azure Key Vault</span></span>

<span data-ttu-id="cffa1-117">デジタル署名拡張機能は、Retail Serverが配置されているマシンのローカルの証明書のストレージにインストールされている証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-117">The digital signature extension uses a certificate that is installed in the local certificate storage of the machine where Retail Server is deployed.</span></span> <span data-ttu-id="cffa1-118">コンフィギュレーション ファイルの証明書の拇印を指定する必要があります (このトピックで後述する [SequentialSignatureRegisterコンポーネント](#sequentialsignatureregister-component) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="cffa1-118">The thumbprint of the certificate must be specified in the configuration file (see the [SequentialSignatureRegister component](#sequentialsignatureregister-component) section later in this topic).</span></span> <span data-ttu-id="cffa1-119">実装のトポロジーに応じて、証明書は [Microsoft Azure Key Vault ストレージ](https://docs.microsoft.com/azure/key-vault/key-vault-get-started) に保存される必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-119">Depending on the implementation topology, the certificate might have to be stored in [Microsoft Azure Key Vault storage](https://docs.microsoft.com/azure/key-vault/key-vault-get-started).</span></span> <span data-ttu-id="cffa1-120">フランス用ローカライズには、Azure Key Vault ストレージに保存されている証明書を使用して、署名フローを上書きし、販売取引に署名する方法を示すサンプル コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cffa1-120">The localization for France contains a code sample that shows how to override the signing flow and sign sales transactions by using a certificate that is stored in Azure Key Vault storage.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cffa1-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="cffa1-121">Prerequisites</span></span>

<span data-ttu-id="cffa1-122">Azure Key Vault ストレージに格納されている証明書を使用する前に、次の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-122">The following steps must be completed before you can use a certificate that is stored in Azure Key Vault storage:</span></span>

- <span data-ttu-id="cffa1-123">Azure Key Vault ストレージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-123">The Azure Key Vault storage must be created.</span></span> <span data-ttu-id="cffa1-124">Retail Server と同じ地理的領域にストレージを配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-124">We recommend that you deploy the storage in the same geographical region as the Retail Server.</span></span>
- <span data-ttu-id="cffa1-125">証明書は、そのストレージにアップロードされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-125">The certificate must be uploaded to the storage.</span></span>
- <span data-ttu-id="cffa1-126">ストレージから機密情報を読み取るには、Retail Server アプリケーションが承認される必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-126">The Retail Server application must be authorized to read secrets from the storage.</span></span>

<span data-ttu-id="cffa1-127">Azure Key Vault を操作する方法の詳細については、次を参照してください。[Azure Key Vault の使用を開始します](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)。</span><span class="sxs-lookup"><span data-stu-id="cffa1-127">For more information about how to work with Azure Key Vault, see [Get started with Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-get-started).</span></span>

### <a name="using-the-sample"></a><span data-ttu-id="cffa1-128">サンプルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-128">Using the sample</span></span>

<span data-ttu-id="cffa1-129">**DigitalSignatureKeyVaultSample** プロジェクトは、Azure Key Vault ストレージに格納されている証明書を使用するためのサンプル コードを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-129">The **DigitalSignatureKeyVaultSample** project contains sample code that uses a certificate that is stored in Azure Key Vault storage.</span></span> <span data-ttu-id="cffa1-130">サンプルを実稼働環境で使用するには、ロジックを実装し、**CertificateSignatureServiceRequestHandler** クラスにある **HashAndSignData** メソッドで、次のパラメータを指定できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-130">To use the sample in a production environment, you must implement logic so that the following parameters can be specified in the **HashAndSignData** method of the **CertificateSignatureServiceRequestHandler** class:</span></span>

- <span data-ttu-id="cffa1-131">**Azure Key Vault URL** - Azure Key Vault ストレージの URL。</span><span class="sxs-lookup"><span data-stu-id="cffa1-131">**Azure Key Vault URL** – The URL of the Azure Key Vault storage.</span></span>

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultUrl, "Set your Azure Key Vault URL here");
    ```

- <span data-ttu-id="cffa1-132">**クライアント ID** - 認証のために Azure Key Vault ストレージに関連付けられている Azure Active Directory (Azure AD) アプリケーションのインタラクティブ クライアント ID。</span><span class="sxs-lookup"><span data-stu-id="cffa1-132">**Client ID** – An interactive client ID of the Azure Active Directory (Azure AD) application that is associated with the Azure Key Vault storage for authentication purposes.</span></span> <span data-ttu-id="cffa1-133">このクライアントは、 Azure Key Vault ストレージから機密情報を読み取るためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="cffa1-133">This client should have access to read secrets from the Azure Key Vault storage.</span></span>

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultInteractiveClientId, "Set the client ID here");
    ```

- <span data-ttu-id="cffa1-134">**クライアント シークレット** - Azure Key Vault ストレージで認証のために使用される Azure AD アプリケーションと関連している秘密キー。</span><span class="sxs-lookup"><span data-stu-id="cffa1-134">**Client secret** – A secret key that is associated with the Azure AD application that is used for authentication in the Azure Key Vault storage.</span></span>

    ``` csharp
    // Secret key value should be encrypted and stored in a safe place.
    settings.Add(WellKnownKeyVaultSettings.KeyVaultClientSecretKey, "Set the secret key here");
    ```

- <span data-ttu-id="cffa1-135">**秘密参照**- 証明書への秘密の参照。</span><span class="sxs-lookup"><span data-stu-id="cffa1-135">**Secret reference** – A secret reference to the certificate.</span></span>

    ``` csharp
    SecretCertificate secretCertificate = settingsHelper.SecretProvider.GetSecret("vault:///{Specify the secret reference}") as SecretCertificate;
    ```

<span data-ttu-id="cffa1-136">署名のフローを上書きする場合は以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-136">To override the signing flow, follow these steps.</span></span>

1. <span data-ttu-id="cffa1-137">**DigitalSignatureKeyVaultSample** プロジェクトを構築し、、**Contoso.Commerce.Runtime.DigitalSignatureKeyVaultSample.dll** アセンブリを **bin\\ext** Retail Server folder にコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-137">Build the **DigitalSignatureKeyVaultSample** project, and copy the **Contoso.Commerce.Runtime.DigitalSignatureKeyVaultSample.dll** assembly to the **bin\\ext** Retail Server folder.</span></span>
2. <span data-ttu-id="cffa1-138">**コンポジション** セクションに次の行を追加して、**commerceRuntime.ext.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-138">Update the **commerceRuntime.ext.config** file by adding the following line to the **composition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
    ```

> [!NOTE]
> <span data-ttu-id="cffa1-139">デジタル署名に使用される証明書の拇印は、証明書が Azure Key Vault ストレージに保存されている場合でも、SequentialSignatureRegister アセンブリのコンフィギュレーション ファイルで指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-139">The thumbprint of the certificate that is used for digital signing should be specified in the configuration file of the SequentialSignatureRegister assembly, even if the certificate is stored in Azure Key Vault storage.</span></span> <span data-ttu-id="cffa1-140">詳細については、このトピックの後半の [SequentialSignatureRegister コンポーネント](#sequentialsignatureregister-component) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-140">For more information, see the [SequentialSignatureRegister component](#sequentialsignatureregister-component) section later in this topic.</span></span>

## <a name="specifying-application-attributes-that-will-be-printed-on-receipts"></a><span data-ttu-id="cffa1-141">レシートに印刷されるアプリケーション属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-141">Specifying application attributes that will be printed on receipts</span></span>

<span data-ttu-id="cffa1-142">カスタム フィールドを使用することで、次のようなアプリケーション属性をレシートに印刷できます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-142">You can use custom fields to print the following application attributes on receipts</span></span><!-- (for more information, see [Cash registers for France](./emea-fra-cash-registers.md))--><span data-ttu-id="cffa1-143">:</span><span class="sxs-lookup"><span data-stu-id="cffa1-143">:</span></span>

- <span data-ttu-id="cffa1-144">**ビルド番号**- POS アプリケーションのソフトウェアのバージョン。</span><span class="sxs-lookup"><span data-stu-id="cffa1-144">**Build number** – The software version of the POS application.</span></span> <span data-ttu-id="cffa1-145">既定では、この値は、Microsoft が POS アプリケーションに割り当てた POS ビルド番号と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-145">By default, the value should equal the POS build number that Microsoft assigned to the POS application.</span></span>
- <span data-ttu-id="cffa1-146">**証明書のカテゴリ**および**証明書の番号** - アプリケーションの認定証明を発行するカテゴリとコンプライアンスの証明書の数。</span><span class="sxs-lookup"><span data-stu-id="cffa1-146">**Certificate category** and **Certificate number** – The category and number of the certificate of compliance that an accredited body issues for the application.</span></span> <span data-ttu-id="cffa1-147">既定では、値はカテゴリとMicrosoft に与えられた証明書の数に等しい。</span><span class="sxs-lookup"><span data-stu-id="cffa1-147">By default, the values equal the category and the number of the certificate that is granted to Microsoft:</span></span>

    - <span data-ttu-id="cffa1-148">Microsoft Dynamics 365 for Commerce:</span><span class="sxs-lookup"><span data-stu-id="cffa1-148">Microsoft Dynamics 365 for Commerce:</span></span>

        - <span data-ttu-id="cffa1-149">**証明書のカテゴリ:** C</span><span class="sxs-lookup"><span data-stu-id="cffa1-149">**Certificate category:** C</span></span>
        - <span data-ttu-id="cffa1-150">**証明書番号:** 18/0202</span><span class="sxs-lookup"><span data-stu-id="cffa1-150">**Certificate number:** 18/0202</span></span>

    - <span data-ttu-id="cffa1-151">Microsoft Dynamics 365 for Commerce:</span><span class="sxs-lookup"><span data-stu-id="cffa1-151">Microsoft Dynamics 365 for Commerce:</span></span>

        - <span data-ttu-id="cffa1-152">**証明書のカテゴリ:** B</span><span class="sxs-lookup"><span data-stu-id="cffa1-152">**Certificate category:** B</span></span>
        - <span data-ttu-id="cffa1-153">**証明書番号:** 18/0203</span><span class="sxs-lookup"><span data-stu-id="cffa1-153">**Certificate number:** 18/0203</span></span>

    > [!NOTE]
    > <span data-ttu-id="cffa1-154">既定では、証明書のカテゴリおよび割り当てられている番号が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-154">By default, the certificate category and number that are assigned are printed.</span></span> <span data-ttu-id="cffa1-155">コマースを実装している場合は、証明書のカテゴリと番号を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-155">If you're implementing Commerce, you must override the certificate category and number.</span></span>

<span data-ttu-id="cffa1-156">POS アプリケーションをカスタマイズしていて、そのカスタマイズがアプリケーションのコンプライアンスに影響を与える場合は、認定機関にコンプライアンスの新しい証明書を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-156">If you customize the POS application, and your customizations affect the compliance of the application, you might have to request a new certificate of compliance from an accredited body.</span></span> <span data-ttu-id="cffa1-157">この場合、ビルド番号、および証明書のカテゴリ、および番号を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-157">In this case, you must override the build number, and the certificate category and number.</span></span> <span data-ttu-id="cffa1-158">それ以外の場合、証明書のカテゴリおよび番号の既定値が印刷されますが、Microsoft が POS アプリケーションに割り当てた POS ビルド番号も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-158">Otherwise, the default values for the certificate category and number will be printed, but you must still specify the POS build number that Microsoft assigned to the POS application.</span></span>

### <a name="overriding-the-build-number"></a><span data-ttu-id="cffa1-159">ビルド番号の変更</span><span class="sxs-lookup"><span data-stu-id="cffa1-159">Overriding the build number</span></span>

<span data-ttu-id="cffa1-160">ソフトウェアのバージョン/ビルド番号と発行元は、**RetailSDK\\BuildTools\\Customization.settings** で指定されます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-160">The software version/build number and publisher are specified in **RetailSDK\\BuildTools\\Customization.settings**.</span></span>

```xml
<CustomVersion Condition="'$(CustomVersion)' == ''">1.0.0.1</CustomVersion>
<CustomName Condition="'$(CustomName)' == ''">Contoso Retail Customization</CustomName> 
<CustomDescription Condition="'$(CustomDescription)' == ''">Contoso Retail Customization</CustomDescription>
<CustomPublisher Condition="'$(CustomPublisher)' == ''">CN=Contoso Ltd.</CustomPublisher>
<CustomPublisherDisplayName Condition="'$(CustomPublisherDisplayName)' == ''">Contoso Ltd.</CustomPublisherDisplayName>
<CustomCopyright Condition="'$(CustomCopyright)' == ''">Copyright © 2016</CustomCopyright>
```

### <a name="overriding-the-certificate-category-and-number"></a><span data-ttu-id="cffa1-161">証明書のカテゴリや番号の変更</span><span class="sxs-lookup"><span data-stu-id="cffa1-161">Overriding the certificate category and number</span></span>

<span data-ttu-id="cffa1-162">証明書のカテゴリと番号は、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsFrance\\GetSalesTransactionCustomReceiptFieldService** で指定されます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-162">The certificate category and number are specified in **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsFrance\\GetSalesTransactionCustomReceiptFieldService**.</span></span>

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
> <span data-ttu-id="cffa1-163">コマースを実装している場合は、証明書のカテゴリと番号も上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-163">You must also override the certificate category and number if you're implementing Commerce.</span></span> <span data-ttu-id="cffa1-164">この場合、このトピックで先に見たセクション、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) にある証明書のカテゴリおよびに記載されている証明書のカテゴリと番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-164">In this case, use the certificate category and number that are provided in the [Specifying application attributes that will be printed on receipts](#specifying-application-attributes-that-will-be-printed-on-receipts) section earlier in this topic.</span></span>

## <a name="development-environment"></a><span data-ttu-id="cffa1-165">開発環境</span><span class="sxs-lookup"><span data-stu-id="cffa1-165">Development environment</span></span>

<span data-ttu-id="cffa1-166">次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-166">Follow these steps to set up a development environment so that you can test and extend the localization functionality.</span></span>

### <a name="crt-extension-components"></a><span data-ttu-id="cffa1-167">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-167">CRT extension components</span></span>

<span data-ttu-id="cffa1-168">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-168">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="cffa1-169">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-169">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="commonfrance-component"></a><span data-ttu-id="cffa1-170">CommonFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-170">CommonFrance component</span></span>

1. <span data-ttu-id="cffa1-171">**Runtime.Extensions.CommonFrance** プロジェクトを見つけ、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-171">Find the **Runtime.Extensions.CommonFrance** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-172">**Extensions.CommonFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.CommonFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-172">In the **Extensions.CommonFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.CommonFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-173">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-173">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-174">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-174">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-175">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-175">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="cffa1-176">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-176">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-177">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-177">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-178">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-178">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="cffa1-179">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-179">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
    ```

#### <a name="receiptsfrance-component"></a><span data-ttu-id="cffa1-180">ReceiptsFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-180">ReceiptsFrance component</span></span>

1. <span data-ttu-id="cffa1-181">**Runtime.Extensions.ReceiptsFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-181">Find the **Runtime.Extensions.ReceiptsFrance** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-182">**Extensions.ReceiptsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-182">In the **Extensions.ReceiptsFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-183">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-183">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-184">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-184">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-185">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-185">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="cffa1-186">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-186">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-187">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-187">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-188">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-188">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="cffa1-189">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-189">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
    ```

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="cffa1-190">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-190">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="cffa1-191">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-191">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-192">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-192">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-193">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-193">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-194">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-194">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-195">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-195">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="cffa1-196">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-196">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-197">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-197">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-198">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-198">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="cffa1-199">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-199">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

#### <a name="salespaymenttransextfrance-component"></a><span data-ttu-id="cffa1-200">SalesPaymentTransExtFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-200">SalesPaymentTransExtFrance component</span></span>

1. <span data-ttu-id="cffa1-201">**Runtime.Extensions.SalesPaymentTransExtFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-201">Find the **Runtime.Extensions.SalesPaymentTransExtFrance** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-202">**Extensions.SalesPaymentTransExtFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-202">In the **Extensions.SalesPaymentTransExtFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-203">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-203">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-204">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-204">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-205">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-205">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="cffa1-206">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-206">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-207">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-207">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-208">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-208">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="cffa1-209">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-209">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
    ```

#### <a name="sequentialsignaturefrance-component"></a><span data-ttu-id="cffa1-210">SequentialSignatureFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-210">SequentialSignatureFrance component</span></span>

1. <span data-ttu-id="cffa1-211">**Runtime.Extensions.SequentialSignatureFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-211">Find the **Runtime.Extensions.SequentialSignatureFrance** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-212">**Extensions.SequentialSignatureFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-212">In the **Extensions.SequentialSignatureFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-213">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-213">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-214">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-214">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-215">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-215">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="cffa1-216">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-216">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-217">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-217">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-218">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-218">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="cffa1-219">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-219">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
    ```

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="cffa1-220">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-220">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="cffa1-221">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-221">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="cffa1-222">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-222">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="cffa1-223">**CertificateThumbprint** プロパティは、唯一の必須のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="cffa1-223">The **certificateThumbprint** property is the only mandatory property.</span></span> <span data-ttu-id="cffa1-224">この値は必ず文字列で、40 字の長さがあり、大文字で、区切り記号を含みません。</span><span class="sxs-lookup"><span data-stu-id="cffa1-224">The value must be a string that is 40 characters long in upper case and that doesn't include any delimiters.</span></span> <span data-ttu-id="cffa1-225">詳細については、[証明書の拇印を取得する方法](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-225">For more information, see [How to retrieve the thumbprint of a certificate](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate).</span></span>

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

3. <span data-ttu-id="cffa1-226">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-226">Build the project.</span></span>
4. <span data-ttu-id="cffa1-227">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-227">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="cffa1-228">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="cffa1-228">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="cffa1-229">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="cffa1-229">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="cffa1-230">ファイルを CRT 拡張フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-230">Copy the files to the CRT extension folder:</span></span>

    - <span data-ttu-id="cffa1-231">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-231">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-232">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-232">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="cffa1-233">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-233">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-234">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-234">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-235">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-235">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="cffa1-236">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-236">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="cffa1-237">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-237">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="cffa1-238">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-238">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-239">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-239">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-240">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-240">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-241">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-241">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-242">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-242">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="xzreportsfrance-component"></a><span data-ttu-id="cffa1-243">XZReportsFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-243">XZReportsFrance component</span></span>

1. <span data-ttu-id="cffa1-244">**Runtime.Extensions.XZReportsFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-244">Find the **Runtime.Extensions.XZReportsFrance** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-245">**Extensions.XZReportsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-245">In the **Extensions.XZReportsFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-246">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-246">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-247">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-247">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-248">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-248">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="cffa1-249">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-249">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-250">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-250">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-251">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-251">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="cffa1-252">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-252">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
    ```

#### <a name="restrictingshiftduration-component"></a><span data-ttu-id="cffa1-253">RestrictingShiftDuration コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-253">RestrictingShiftDuration component</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-254">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-254">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

1. <span data-ttu-id="cffa1-255">**Runtime.Extensions.RestrictingShiftDuration** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-255">Find the **Runtime.Extensions.RestrictingShiftDuration** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-256">**Extensions.RestrictingShiftDuration\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RestrictingShiftDuration.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-256">In the **Extensions.RestrictingShiftDuration\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RestrictingShiftDuration.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-257">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-257">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="cffa1-258">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-258">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-259">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-259">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="cffa1-260">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-260">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-261">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-261">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-262">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-262">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="cffa1-263">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-263">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RestrictingShiftDuration" />
    ```

# <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-264">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-264">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

1. <span data-ttu-id="cffa1-265">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-265">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-266">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-266">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-267">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-267">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="cffa1-268">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-268">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    ```

# <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-269">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-269">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

1. <span data-ttu-id="cffa1-270">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-270">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="cffa1-271">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-271">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="cffa1-272">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-272">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="cffa1-273">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-273">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    ```

---

### <a name="retail-server-extension-components"></a><span data-ttu-id="cffa1-274">Retail Server 拡張機能コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-274">Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="cffa1-275">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-275">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="cffa1-276">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-276">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-277">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-277">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="cffa1-278">IIS Retail Server サイトの場所の **\\bin\\ext** フォルダーにアセンブリ ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-278">Copy the assembly file to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
4. <span data-ttu-id="cffa1-279">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-279">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="cffa1-280">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-280">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>
5. <span data-ttu-id="cffa1-281">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-281">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

### <a name="proxy-extension-component"></a><span data-ttu-id="cffa1-282">プロキシ拡張機能コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-282">Proxy extension component</span></span>

<span data-ttu-id="cffa1-283">Modern POS に対してオフライン モードで拡張機能を有効にする次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-283">You must complete the following procedure to enable the extensions in offline mode for Modern POS.</span></span>

#### <a name="salestransactionsignature-retail-proxy-sample-component"></a><span data-ttu-id="cffa1-284">SalesTransactionSignature Retail プロキシ サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-284">SalesTransactionSignature Retail proxy sample component</span></span>

1. <span data-ttu-id="cffa1-285">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-285">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="cffa1-286">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-286">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>
3. <span data-ttu-id="cffa1-287">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-287">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="cffa1-288">拡張機能コンフィギュレーション ファイルで、プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-288">Register the proxy change in the extensions configuration file.</span></span> <span data-ttu-id="cffa1-289">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-289">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

### <a name="modern-pos-extension-components"></a><span data-ttu-id="cffa1-290">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-290">Modern POS extension components</span></span>

1. <span data-ttu-id="cffa1-291">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-291">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="cffa1-292">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-292">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cffa1-293">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-293">Modern POS must not be customized.</span></span> <span data-ttu-id="cffa1-294">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-294">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="cffa1-295">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-295">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-296">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-296">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="cffa1-297">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-297">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-298">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-298">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-299">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-299">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-300">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="cffa1-300">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="cffa1-301">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-301">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-302">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-302">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="cffa1-303">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-303">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-304">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-304">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-305">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-305">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-306">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-306">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-307">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-307">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="cffa1-308">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-308">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-309">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-309">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-310">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-310">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-311">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-311">SalesTransBuildNumberSample</span></span>

    ---

    > [!NOTE]
    > <span data-ttu-id="cffa1-312">プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで**すべてのファイルを表示する** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-312">To view all files in the project folder, not just the files that are included in the project, select the **Show All Files** button in Solution Explorer.</span></span> <span data-ttu-id="cffa1-313">このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-313">If this button isn't available, make sure that you selected the project.</span></span> <span data-ttu-id="cffa1-314">現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-314">The icons of files and folders that aren't currently part of the project have a dotted outline.</span></span> <span data-ttu-id="cffa1-315">プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-315">Right-click the folder to include in the project, and then select **Include in Project**.</span></span>

3. <span data-ttu-id="cffa1-316">**tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-316">Enable the extensions to be compiled by removing the following folders from the exclude list in **tsconfig.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-317">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-317">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="cffa1-318">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-318">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-319">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-319">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-320">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-320">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-321">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="cffa1-321">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="cffa1-322">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-322">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-323">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-323">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="cffa1-324">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-324">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-325">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-325">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-326">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-326">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-327">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-327">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-328">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-328">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="cffa1-329">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-329">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-330">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-330">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-331">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-331">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-332">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-332">SalesTransBuildNumberSample</span></span>

    ---

4. <span data-ttu-id="cffa1-333">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-333">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-334">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-334">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-335">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-335">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-336">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-336">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="cffa1-337">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-337">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="cffa1-338">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-338">Rebuild the solution.</span></span>
6. <span data-ttu-id="cffa1-339">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-339">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="cffa1-340">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cffa1-340">Cloud POS extension components</span></span>

1. <span data-ttu-id="cffa1-341">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-341">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="cffa1-342">**Pos.Extensions** プロジェクトで、既存のソース コードのフォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-342">Include the following existing source code folders in the **Pos.Extensions** project:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-343">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-343">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="cffa1-344">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-344">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-345">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-345">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-346">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-346">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-347">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="cffa1-347">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="cffa1-348">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-348">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-349">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-349">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="cffa1-350">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-350">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-351">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-351">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-352">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-352">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-353">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-353">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-354">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-354">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="cffa1-355">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-355">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-356">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-356">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-357">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-357">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-358">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-358">SalesTransBuildNumberSample</span></span>

    ---

    > [!NOTE]
    > <span data-ttu-id="cffa1-359">プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで**すべてのファイルを表示する** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-359">To view all files in the project folder, not just the files that are included in the project, select the **Show All Files** button in Solution Explorer.</span></span> <span data-ttu-id="cffa1-360">このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-360">If this button isn't available, make sure that you selected the project.</span></span> <span data-ttu-id="cffa1-361">現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-361">The icons of files and folders that aren't currently part of the project have a dotted outline.</span></span> <span data-ttu-id="cffa1-362">プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-362">Right-click the folder to include in the project, and then select **Include in Project**.</span></span>

3. <span data-ttu-id="cffa1-363">**tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-363">Enable the extensions to be compiled by removing the following folders from the exclude list in **tsconfig.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-364">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-364">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="cffa1-365">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-365">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-366">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-366">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-367">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-367">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-368">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="cffa1-368">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="cffa1-369">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-369">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-370">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-370">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="cffa1-371">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-371">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-372">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-372">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-373">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-373">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-374">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-374">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-375">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-375">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="cffa1-376">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-376">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="cffa1-377">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="cffa1-377">SequentialSignature</span></span>
    - <span data-ttu-id="cffa1-378">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-378">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="cffa1-379">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="cffa1-379">SalesTransBuildNumberSample</span></span>

    ---

4. <span data-ttu-id="cffa1-380">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-380">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-381">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-381">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-382">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-382">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-383">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-383">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="cffa1-384">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-384">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="cffa1-385">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-385">Rebuild the solution.</span></span>
6. <span data-ttu-id="cffa1-386">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-386">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="cffa1-387">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-387">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="cffa1-388">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="cffa1-388">Set up required parameters in Headquarters</span></span>

<span data-ttu-id="cffa1-389">詳細については、 [フランスのキャッシュ レジスター機能](./emea-fra-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-389">For more information, see [Cash register functionality for France](./emea-fra-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="cffa1-390">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="cffa1-390">Production environment</span></span>

<span data-ttu-id="cffa1-391">以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-391">Follow these steps to create deployable packages that contain Commerce components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="cffa1-392">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-392">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="cffa1-393">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-393">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="cffa1-394">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-394">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-395">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-395">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-396">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-396">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-397">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-397">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

        <span data-ttu-id="cffa1-398">デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-398">To use a certificate that is stored in Azure Key Vault storage for digital signing, add the following line.</span></span>

        > [!NOTE]
        > <span data-ttu-id="cffa1-399">この明細行を追加する前に、このトピックの前の方にある[Azure Key Vault にデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-399">Before you add this line, complete the steps in the [Storing a certificate for digital signing in Azure Key Vault](#storing-a-certificate-for-digital-signing-in-azure-key-vault) section earlier in this topic.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
        ```

    2. <span data-ttu-id="cffa1-400">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに以下の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-400">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

3. <span data-ttu-id="cffa1-401">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-401">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="cffa1-402">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージにコマース プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-402">Add the following lines to the **ItemGroup** section to include the Commerce proxy extension in the deployable packages.</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

    2. <span data-ttu-id="cffa1-403">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-403">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="cffa1-404">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-404">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="cffa1-405">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-405">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="cffa1-406">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="cffa1-406">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

        <span data-ttu-id="cffa1-407">デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-407">To use a certificate that is stored in Azure Key Vault storage for digital signing, add the following line.</span></span>

        > [!NOTE]
        > <span data-ttu-id="cffa1-408">この明細行を追加する前に、このトピックの前の方にある、[Azure Key Vaultにデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) セクションにある手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-408">Before you add this line, complete the steps in the [Storing a certificate for digital signing in Azure Key Vault](#storing-a-certificate-for-digital-signing-in-azure-key-vault) section, earlier in this topic.</span></span>

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DataSignatureKeyVaultSample.dll" />
        ```

    3. <span data-ttu-id="cffa1-409">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-409">Add the following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages.</span></span>

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

4. <span data-ttu-id="cffa1-410">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-410">Update the Retail Server configuration file.</span></span> <span data-ttu-id="cffa1-411">**RetailSDK\\Packages\\RetailServer\\Code\\ web.config**で、**extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-411">In **RetailSDK\\Packages\\RetailServer\\Code\\web.config**, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

5. <span data-ttu-id="cffa1-412">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-412">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="cffa1-413">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-413">Then copy the configuration file to the **References** folder.</span></span> <span data-ttu-id="cffa1-414">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-414">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>
6. <span data-ttu-id="cffa1-415">ビルド番号、カテゴリ、および必要に応じて、コンプライアンスの証明書の番号を上書きします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-415">Override the build number and the category and number of the certificate of compliance, as required.</span></span> <span data-ttu-id="cffa1-416">詳細については、このトピックの前の方にある、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) セクションにある指示を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-416">For more information, see the instructions in the [Specifying application attributes that will be printed on receipts](#specifying-application-attributes-that-will-be-printed-on-receipts) section earlier in this topic.</span></span>
7. <span data-ttu-id="cffa1-417">Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-417">Start the MSBuild Command Prompt for Visual Studio utility, and run **msbuild** under the Retail SDK folder to create deployable packages.</span></span>
8. <span data-ttu-id="cffa1-418">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-418">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="cffa1-419">詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cffa1-419">For more information, see [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="cffa1-420">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-420">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="cffa1-421">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="cffa1-421">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="cffa1-422">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-422">Sign in to POS.</span></span>
2. <span data-ttu-id="cffa1-423">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-423">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="cffa1-424">**ダウンロードの保留中**フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="cffa1-424">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="cffa1-425">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="cffa1-425">Sign out of POS.</span></span>
4. <span data-ttu-id="cffa1-426">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="cffa1-426">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="cffa1-427">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="cffa1-427">Sign in to POS.</span></span>
6. <span data-ttu-id="cffa1-428">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-428">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="cffa1-429">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="cffa1-429">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="cffa1-430">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="cffa1-430">Restart Modern POS.</span></span>
