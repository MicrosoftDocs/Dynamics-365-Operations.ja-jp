---
title: フランスのキャッシュ レジスターの配置ガイドライン
description: このトピックは、フランスの小売ローカライズ用配置ガイドです。
author: AlexChern0v
manager: ezubov
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: shylaw
ms.search.scope: Retail
ms.search.region: France
ms.search.industry: Retail
ms.author: v-alexec
ms.search.validFrom: 2018-4-13
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: d17d0253cbd719aac8c811e7237c669021aca889
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369447"
---
# <a name="deployment-guidelines-for-cash-registers-for-france"></a><span data-ttu-id="ae395-103">フランスのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ae395-103">Deployment guidelines for cash registers for France</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ae395-104">このトピックは、Microsoft Dynamics 365 for Retail のフランスでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="ae395-104">This topic is a deployment guide that shows how to enable the Microsoft Dynamics 365 for Retail localization for France.</span></span> <span data-ttu-id="ae395-105">ローカライズは、小売コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="ae395-105">The localization consists of several extensions of Retail components.</span></span> <span data-ttu-id="ae395-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="ae395-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="ae395-107">フランスの小売ローカライズの詳細については、[フランスのキャッシュ レジスター](./emea-fra-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-107">For more information about the Retail localization for France, see [Cash registers for France](./emea-fra-cash-registers.md).</span></span>

<span data-ttu-id="ae395-108">このローカライズは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="ae395-108">This localization is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="ae395-109">リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-109">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="ae395-110">このローカライズは、Commerce runtime (CRT)、Retail Servers、および POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="ae395-110">This localization consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="ae395-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="ae395-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae395-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="ae395-113">また Microsoft Visual Studio オンライン (VSO) のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae395-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

## <a name="storing-a-certificate-for-digital-signing-in-azure-key-vault"></a><span data-ttu-id="ae395-114">Azure Key Vault にデジタル署名用証明書を保存します。</span><span class="sxs-lookup"><span data-stu-id="ae395-114">Storing a certificate for digital signing in Azure Key Vault</span></span>

<span data-ttu-id="ae395-115">デジタル署名拡張機能は、Retail Serverが配置されているマシンのローカルの証明書のストレージにインストールされている証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae395-115">The digital signature extension uses a certificate that is installed in the local certificate storage of the machine where Retail Server is deployed.</span></span> <span data-ttu-id="ae395-116">コンフィギュレーション ファイルの証明書の拇印を指定する必要があります (このトピックで後述する [SequentialSignatureRegisterコンポーネント](#sequentialsignatureregister-component) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="ae395-116">The thumbprint of the certificate must be specified in the configuration file (see the [SequentialSignatureRegister component](#sequentialsignatureregister-component) section later in this topic).</span></span> <span data-ttu-id="ae395-117">実装のトポロジーに応じて、証明書は [Microsoft Azure Key Vault ストレージ](https://docs.microsoft.com/azure/key-vault/key-vault-get-started) に保存される必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-117">Depending on the implementation topology, the certificate might have to be stored in [Microsoft Azure Key Vault storage](https://docs.microsoft.com/azure/key-vault/key-vault-get-started).</span></span> <span data-ttu-id="ae395-118">フランス用小売ローカライズには、Azure Key Vault ストレージに保存されている証明書を使用して、署名フローを上書きし、販売取引に署名する方法を示すサンプル コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ae395-118">The Retail localization for France contains a code sample that shows how to override the signing flow and sign sales transactions by using a certificate that is stored in Azure Key Vault storage.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ae395-119">必要条件</span><span class="sxs-lookup"><span data-stu-id="ae395-119">Prerequisites</span></span>
<span data-ttu-id="ae395-120">Azure Key Vault ストレージに格納されている証明書を使用する前に、次の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-120">The following steps must be completed before you can use a certificate that is stored in Azure Key Vault storage:</span></span>

- <span data-ttu-id="ae395-121">Azure Key Vault ストレージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-121">The Azure Key Vault storage must be created.</span></span> <span data-ttu-id="ae395-122">Retail Server と同じ地理的領域にストレージを配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae395-122">We recommend that you deploy the storage in the same geographical region as the Retail Server.</span></span>
- <span data-ttu-id="ae395-123">証明書は、そのストレージにアップロードされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-123">The certificate must be uploaded to the storage.</span></span>
- <span data-ttu-id="ae395-124">ストレージから機密情報を読み取るには、Retail Server アプリケーションが承認される必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-124">The Retail Server application must be authorized to read secrets from the storage.</span></span>

<span data-ttu-id="ae395-125">Azure Key Vault を操作する方法の詳細については、次を参照してください。[Azure Key Vault の使用を開始します](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)。</span><span class="sxs-lookup"><span data-stu-id="ae395-125">For more information about how to work with Azure Key Vault, see [Get started with Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-get-started).</span></span>

### <a name="using-the-sample"></a><span data-ttu-id="ae395-126">サンプルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-126">Using the sample</span></span>

<span data-ttu-id="ae395-127">**DigitalSignatureKeyVaultSample** プロジェクトは、Azure Key Vault ストレージに格納されている証明書を使用するためのサンプル コードを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="ae395-127">The **DigitalSignatureKeyVaultSample** project contains sample code that uses a certificate that is stored in Azure Key Vault storage.</span></span> <span data-ttu-id="ae395-128">サンプルを実稼働環境で使用するには、ロジックを実装し、**CertificateSignatureServiceRequestHandler** クラスにある **HashAndSignData** メソッドで、次のパラメータを指定できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-128">To use the sample in a production environment, you must implement logic so that the following parameters can be specified in the **HashAndSignData** method of the **CertificateSignatureServiceRequestHandler** class:</span></span>

- <span data-ttu-id="ae395-129">**Azure Key Vault URL** - Azure Key Vault ストレージの URL。</span><span class="sxs-lookup"><span data-stu-id="ae395-129">**Azure Key Vault URL** – The URL of the Azure Key Vault storage.</span></span>

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultUrl, "Set your Azure Key Vault URL here");
    ```

- <span data-ttu-id="ae395-130">**クライアント ID** - 認証のために Azure Key Vault ストレージに関連付けられている Azure Active Directory (Azure AD) アプリケーションのインタラクティブ クライアント ID。</span><span class="sxs-lookup"><span data-stu-id="ae395-130">**Client ID** – An interactive client ID of the Azure Active Directory (Azure AD) application that is associated with the Azure Key Vault storage for authentication purposes.</span></span> <span data-ttu-id="ae395-131">このクライアントは、 Azure Key Vault ストレージから機密情報を読み取るためのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="ae395-131">This client should have access to read secrets from the Azure Key Vault storage.</span></span>

    ``` csharp
    settings.Add(WellKnownKeyVaultSettings.KeyVaultInteractiveClientId, "Set the client ID here");
    ```

- <span data-ttu-id="ae395-132">**クライアント シークレット** - Azure Key Vault ストレージで認証のために使用される Azure AD アプリケーションと関連している秘密キー。</span><span class="sxs-lookup"><span data-stu-id="ae395-132">**Client secret** – A secret key that is associated with the Azure AD application that is used for authentication in the Azure Key Vault storage.</span></span>

    ``` csharp
    // Secret key value should be encrypted and stored in a safe place.
    settings.Add(WellKnownKeyVaultSettings.KeyVaultClientSecretKey, "Set the secret key here");
    ```

- <span data-ttu-id="ae395-133">**秘密参照**- 証明書への秘密の参照。</span><span class="sxs-lookup"><span data-stu-id="ae395-133">**Secret reference** – A secret reference to the certificate.</span></span>

    ``` csharp
    SecretCertificate secretCertificate = settingsHelper.SecretProvider.GetSecret("vault:///{Specify the secret reference}") as SecretCertificate;
    ```

<span data-ttu-id="ae395-134">署名のフローを上書きする場合は以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ae395-134">To override the signing flow, follow these steps.</span></span>

1. <span data-ttu-id="ae395-135">**DigitalSignatureKeyVaultSample** プロジェクトを構築し、、**Contoso.Commerce.Runtime.DigitalSignatureKeyVaultSample.dll** アセンブリを **bin\\ext** Retail Server folder にコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-135">Build the **DigitalSignatureKeyVaultSample** project, and copy the **Contoso.Commerce.Runtime.DigitalSignatureKeyVaultSample.dll** assembly to the **bin\\ext** Retail Server folder.</span></span>
2. <span data-ttu-id="ae395-136">**コンポジション** セクションに次の行を追加して、**commerceRuntime.ext.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="ae395-136">Update the **commerceRuntime.ext.config** file by adding the following line to the **composition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
    ```

> [!NOTE]
> <span data-ttu-id="ae395-137">デジタル署名に使用される証明書の拇印は、証明書が Azure Key Vault ストレージに保存されている場合でも、SequentialSignatureRegister アセンブリのコンフィギュレーション ファイルで指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-137">The thumbprint of the certificate that is used for digital signing should be specified in the configuration file of the SequentialSignatureRegister assembly, even if the certificate is stored in Azure Key Vault storage.</span></span> <span data-ttu-id="ae395-138">詳細については、このトピックの後半の [SequentialSignatureRegister コンポーネント](#sequentialsignatureregister-component) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-138">For more information, see the [SequentialSignatureRegister component](#sequentialsignatureregister-component) section later in this topic.</span></span>

## <a name="specifying-application-attributes-that-will-be-printed-on-receipts"></a><span data-ttu-id="ae395-139">レシートに印刷されるアプリケーション属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae395-139">Specifying application attributes that will be printed on receipts</span></span>

<span data-ttu-id="ae395-140">カスタム フィールドを使用して、次のようなアプリケーション属性をレシートに印刷<!-- (for more information, see [Cash registers for France](./emea-fra-cash-registers.md))-->できます。</span><span class="sxs-lookup"><span data-stu-id="ae395-140">You can use custom fields to print the following application attributes on receipts<!-- (for more information, see [Cash registers for France](./emea-fra-cash-registers.md))-->:</span></span>

- <span data-ttu-id="ae395-141">**ビルド番号**- POS アプリケーションのソフトウェアのバージョン。</span><span class="sxs-lookup"><span data-stu-id="ae395-141">**Build number** – The software version of the POS application.</span></span> <span data-ttu-id="ae395-142">既定では、この値は、Microsoft が POS アプリケーションに割り当てた POS ビルド番号と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="ae395-142">By default, the value should equal the POS build number that Microsoft assigned to the POS application.</span></span>
- <span data-ttu-id="ae395-143">**証明書のカテゴリ**および**証明書の番号** - アプリケーションの認定証明を発行するカテゴリとコンプライアンスの証明書の数。</span><span class="sxs-lookup"><span data-stu-id="ae395-143">**Certificate category** and **Certificate number** – The category and number of the certificate of compliance that an accredited body issues for the application.</span></span> <span data-ttu-id="ae395-144">既定では、値はカテゴリとMicrosoft に与えられた証明書の数に等しい。</span><span class="sxs-lookup"><span data-stu-id="ae395-144">By default, the values equal the category and the number of the certificate that is granted to Microsoft:</span></span>

    - <span data-ttu-id="ae395-145">Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="ae395-145">Microsoft Dynamics 365 for Finance and Operations:</span></span>

        - <span data-ttu-id="ae395-146">**証明書のカテゴリ:** C</span><span class="sxs-lookup"><span data-stu-id="ae395-146">**Certificate category:** C</span></span>
        - <span data-ttu-id="ae395-147">**証明書番号:** 18/0202</span><span class="sxs-lookup"><span data-stu-id="ae395-147">**Certificate number:** 18/0202</span></span>

    - <span data-ttu-id="ae395-148">Microsoft Dynamics 365 for Retail:</span><span class="sxs-lookup"><span data-stu-id="ae395-148">Microsoft Dynamics 365 for Retail:</span></span>

        - <span data-ttu-id="ae395-149">**証明書のカテゴリ:** B</span><span class="sxs-lookup"><span data-stu-id="ae395-149">**Certificate category:** B</span></span>
        - <span data-ttu-id="ae395-150">**証明書番号:** 18/0203</span><span class="sxs-lookup"><span data-stu-id="ae395-150">**Certificate number:** 18/0203</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae395-151">既定では、証明書のカテゴリとFinance and Operationsに割り当てられている番号が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="ae395-151">By default, the certificate category and number that are assigned to Finance and Operations are printed.</span></span> <span data-ttu-id="ae395-152">小売を実装する場合は、証明書のカテゴリと番号を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-152">If you're implementing Retail, you must override the certificate category and number.</span></span>

<span data-ttu-id="ae395-153">POS アプリケーションをカスタマイズしていて、そのカスタマイズがアプリケーションのコンプライアンスに影響を与える場合は、認定機関にコンプライアンスの新しい証明書を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-153">If you customize the POS application, and your customizations affect the compliance of the application, you might have to request a new certificate of compliance from an accredited body.</span></span> <span data-ttu-id="ae395-154">この場合、ビルド番号、および証明書のカテゴリ、および番号を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-154">In this case, you must override the build number, and the certificate category and number.</span></span> <span data-ttu-id="ae395-155">それ以外の場合、証明書のカテゴリおよび番号の既定値が印刷されますが、Microsoft が POS アプリケーションに割り当てた POS ビルド番号も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-155">Otherwise, the default values for the certificate category and number will be printed, but you must still specify the POS build number that Microsoft assigned to the POS application.</span></span>

### <a name="overriding-the-build-number"></a><span data-ttu-id="ae395-156">ビルド番号の変更</span><span class="sxs-lookup"><span data-stu-id="ae395-156">Overriding the build number</span></span>

<span data-ttu-id="ae395-157">ソフトウェアのバージョン/ビルド番号と発行元は、**RetailSDK\\BuildTools\\Customization.settings** で指定されます。</span><span class="sxs-lookup"><span data-stu-id="ae395-157">The software version/build number and publisher are specified in **RetailSDK\\BuildTools\\Customization.settings**.</span></span>

```xml
<CustomVersion Condition="'$(CustomVersion)' == ''">1.0.0.1</CustomVersion>
<CustomName Condition="'$(CustomName)' == ''">Contoso Retail Customization</CustomName> 
<CustomDescription Condition="'$(CustomDescription)' == ''">Contoso Retail Customization</CustomDescription>
<CustomPublisher Condition="'$(CustomPublisher)' == ''">CN=Contoso Ltd.</CustomPublisher>
<CustomPublisherDisplayName Condition="'$(CustomPublisherDisplayName)' == ''">Contoso Ltd.</CustomPublisherDisplayName>
<CustomCopyright Condition="'$(CustomCopyright)' == ''">Copyright © 2016</CustomCopyright>
```

### <a name="overriding-the-certificate-category-and-number"></a><span data-ttu-id="ae395-158">証明書のカテゴリや番号の変更</span><span class="sxs-lookup"><span data-stu-id="ae395-158">Overriding the certificate category and number</span></span>

<span data-ttu-id="ae395-159">証明書のカテゴリと番号は、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsFrance\\GetSalesTransactionCustomReceiptFieldService** で指定されます。</span><span class="sxs-lookup"><span data-stu-id="ae395-159">The certificate category and number are specified in **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsFrance\\GetSalesTransactionCustomReceiptFieldService**.</span></span>

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
> <span data-ttu-id="ae395-160">小売を実装する場合は、証明書のカテゴリと番号を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-160">You must also override the certificate category and number if you're implementing Retail.</span></span> <span data-ttu-id="ae395-161">この場合、このトピックで先に見たセクション、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) にある証明書のカテゴリおよびに記載されている証明書のカテゴリと番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae395-161">In this case, use the certificate category and number that are provided in the [Specifying application attributes that will be printed on receipts](#specifying-application-attributes-that-will-be-printed-on-receipts) section earlier in this topic.</span></span>

## <a name="development-environment"></a><span data-ttu-id="ae395-162">開発環境</span><span class="sxs-lookup"><span data-stu-id="ae395-162">Development environment</span></span>

<span data-ttu-id="ae395-163">次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ae395-163">Follow these steps to set up a development environment so that you can test and extend the localization functionality.</span></span>

### <a name="crt-extension-components"></a><span data-ttu-id="ae395-164">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-164">CRT extension components</span></span>

<span data-ttu-id="ae395-165">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae395-165">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="ae395-166">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="ae395-166">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="commonfrance-component"></a><span data-ttu-id="ae395-167">CommonFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-167">CommonFrance component</span></span>

1. <span data-ttu-id="ae395-168">**Runtime.Extensions.CommonFrance** プロジェクトを見つけ、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-168">Find the **Runtime.Extensions.CommonFrance** project, and build it.</span></span>
2. <span data-ttu-id="ae395-169">**Extensions.CommonFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.CommonFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-169">In the **Extensions.CommonFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.CommonFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-170">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-170">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-171">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-171">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-172">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-172">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="ae395-173">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-173">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-174">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-174">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-175">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-175">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="ae395-176">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-176">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.CommonFrance" />
    ```

#### <a name="receiptsfrance-component"></a><span data-ttu-id="ae395-177">ReceiptsFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-177">ReceiptsFrance component</span></span>

1. <span data-ttu-id="ae395-178">**Runtime.Extensions.ReceiptsFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-178">Find the **Runtime.Extensions.ReceiptsFrance** project, and build it.</span></span>
2. <span data-ttu-id="ae395-179">**Extensions.ReceiptsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-179">In the **Extensions.ReceiptsFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-180">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-180">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-181">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-181">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-182">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-182">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="ae395-183">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-183">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-184">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-184">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-185">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-185">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="ae395-186">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-186">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsFrance" />
    ```

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="ae395-187">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-187">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="ae395-188">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-188">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="ae395-189">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-189">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-190">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-190">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-191">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-191">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-192">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-192">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="ae395-193">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-193">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-194">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-194">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-195">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-195">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="ae395-196">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-196">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

#### <a name="salespaymenttransextfrance-component"></a><span data-ttu-id="ae395-197">SalesPaymentTransExtFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-197">SalesPaymentTransExtFrance component</span></span>

1. <span data-ttu-id="ae395-198">**Runtime.Extensions.SalesPaymentTransExtFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-198">Find the **Runtime.Extensions.SalesPaymentTransExtFrance** project, and build it.</span></span>
2. <span data-ttu-id="ae395-199">**Extensions.SalesPaymentTransExtFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-199">In the **Extensions.SalesPaymentTransExtFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-200">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-200">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-201">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-201">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-202">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-202">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="ae395-203">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-203">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-204">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-204">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-205">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-205">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="ae395-206">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-206">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtFrance" />
    ```

#### <a name="sequentialsignaturefrance-component"></a><span data-ttu-id="ae395-207">SequentialSignatureFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-207">SequentialSignatureFrance component</span></span>

1. <span data-ttu-id="ae395-208">**Runtime.Extensions.SequentialSignatureFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-208">Find the **Runtime.Extensions.SequentialSignatureFrance** project, and build it.</span></span>
2. <span data-ttu-id="ae395-209">**Extensions.SequentialSignatureFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-209">In the **Extensions.SequentialSignatureFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-210">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-210">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-211">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-211">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-212">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-212">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="ae395-213">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-213">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-214">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-214">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-215">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-215">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="ae395-216">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-216">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureFrance" />
    ```

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="ae395-217">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-217">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="ae395-218">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-218">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="ae395-219">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="ae395-219">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="ae395-220">**CertificateThumbprint** プロパティは、唯一の必須のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="ae395-220">The **certificateThumbprint** property is the only mandatory property.</span></span> <span data-ttu-id="ae395-221">この値は必ず文字列で、40 字の長さがあり、大文字で、区切り記号を含みません。</span><span class="sxs-lookup"><span data-stu-id="ae395-221">The value must be a string that is 40 characters long in upper case and that doesn't include any delimiters.</span></span> <span data-ttu-id="ae395-222">詳細については、[証明書の拇印を取得する方法](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-222">For more information, see [How to retrieve the thumbprint of a certificate](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate).</span></span>

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

3. <span data-ttu-id="ae395-223">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-223">Build the project.</span></span>
4. <span data-ttu-id="ae395-224">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-224">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="ae395-225">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="ae395-225">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="ae395-226">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="ae395-226">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="ae395-227">ファイルを CRT 拡張フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-227">Copy the files to the CRT extension folder:</span></span>

    - <span data-ttu-id="ae395-228">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-228">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-229">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-229">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="ae395-230">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-230">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-231">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-231">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-232">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-232">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="ae395-233">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-233">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="ae395-234">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-234">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="ae395-235">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-235">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project, and build it.</span></span>
2. <span data-ttu-id="ae395-236">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-236">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-237">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-237">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-238">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-238">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-239">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-239">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="xzreportsfrance-component"></a><span data-ttu-id="ae395-240">XZReportsFrance コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-240">XZReportsFrance component</span></span>

1. <span data-ttu-id="ae395-241">**Runtime.Extensions.XZReportsFrance** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-241">Find the **Runtime.Extensions.XZReportsFrance** project, and build it.</span></span>
2. <span data-ttu-id="ae395-242">**Extensions.XZReportsFrance\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsFrance.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-242">In the **Extensions.XZReportsFrance\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsFrance.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-243">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-243">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-244">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-244">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-245">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-245">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="ae395-246">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-246">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-247">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-247">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-248">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-248">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="ae395-249">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-249">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsFrance" />
    ```

#### <a name="restrictingshiftduration-component"></a><span data-ttu-id="ae395-250">RestrictingShiftDuration コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-250">RestrictingShiftDuration component</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-251">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-251">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

1. <span data-ttu-id="ae395-252">**Runtime.Extensions.RestrictingShiftDuration** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-252">Find the **Runtime.Extensions.RestrictingShiftDuration** project, and build it.</span></span>
2. <span data-ttu-id="ae395-253">**Extensions.RestrictingShiftDuration\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RestrictingShiftDuration.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-253">In the **Extensions.RestrictingShiftDuration\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RestrictingShiftDuration.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-254">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-254">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="ae395-255">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-255">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-256">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-256">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="ae395-257">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-257">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="ae395-258">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-258">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="ae395-259">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-259">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="ae395-260">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-260">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RestrictingShiftDuration" />
    ```

# <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-261">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-261">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

> [!NOTE]
> <span data-ttu-id="ae395-262">追加の作業は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ae395-262">No additional actions are required.</span></span>

# <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-263">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-263">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

> [!NOTE]
> <span data-ttu-id="ae395-264">追加の作業は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ae395-264">No additional actions are required.</span></span>

---

### <a name="retail-server-extension-components"></a><span data-ttu-id="ae395-265">Retail Server 拡張機能コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-265">Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="ae395-266">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-266">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="ae395-267">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-267">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="ae395-268">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-268">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="ae395-269">IIS Retail Server サイトの場所の **\\bin\\ext** フォルダーにアセンブリ ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-269">Copy the assembly file to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
4. <span data-ttu-id="ae395-270">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-270">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="ae395-271">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-271">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>
5. <span data-ttu-id="ae395-272">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-272">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

### <a name="retail-proxy-extension-component"></a><span data-ttu-id="ae395-273">Retail プロキシ 拡張機能コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-273">Retail proxy extension component</span></span>

<span data-ttu-id="ae395-274">Modern POS に対してオフライン モードで拡張機能を有効にする次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-274">You must complete the following procedure to enable the extensions in offline mode for Modern POS.</span></span>

#### <a name="salestransactionsignature-retail-proxy-sample-component"></a><span data-ttu-id="ae395-275">SalesTransactionSignature Retail プロキシ サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-275">SalesTransactionSignature Retail proxy sample component</span></span>

1. <span data-ttu-id="ae395-276">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="ae395-276">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="ae395-277">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="ae395-277">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>
3. <span data-ttu-id="ae395-278">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-278">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="ae395-279">拡張機能コンフィギュレーション ファイルで 小売プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="ae395-279">Register the Retail proxy change in the extensions configuration file.</span></span> <span data-ttu-id="ae395-280">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-280">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

### <a name="modern-pos-extension-components"></a><span data-ttu-id="ae395-281">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-281">Modern POS extension components</span></span>

1. <span data-ttu-id="ae395-282">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae395-282">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="ae395-283">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae395-283">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ae395-284">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="ae395-284">Modern POS must not be customized.</span></span> <span data-ttu-id="ae395-285">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-285">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="ae395-286">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="ae395-286">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-287">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-287">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="ae395-288">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-288">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-289">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-289">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-290">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-290">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-291">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="ae395-291">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="ae395-292">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-292">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-293">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-293">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="ae395-294">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-294">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-295">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-295">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-296">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-296">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-297">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-297">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-298">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-298">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="ae395-299">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-299">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-300">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-300">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-301">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-301">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-302">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-302">SalesTransBuildNumberSample</span></span>

    ---

    > [!NOTE]
    > <span data-ttu-id="ae395-303">プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで**すべてのファイルを表示する** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae395-303">To view all files in the project folder, not just the files that are included in the project, select the **Show All Files** button in Solution Explorer.</span></span> <span data-ttu-id="ae395-304">このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-304">If this button isn't available, make sure that you selected the project.</span></span> <span data-ttu-id="ae395-305">現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-305">The icons of files and folders that aren't currently part of the project have a dotted outline.</span></span> <span data-ttu-id="ae395-306">プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae395-306">Right-click the folder to include in the project, and then select **Include in Project**.</span></span>

3. <span data-ttu-id="ae395-307">**tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ae395-307">Enable the extensions to be compiled by removing the following folders from the exclude list in **tsconfig.json**:</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-308">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-308">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="ae395-309">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-309">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-310">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-310">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-311">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-311">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-312">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="ae395-312">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="ae395-313">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-313">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-314">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-314">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="ae395-315">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-315">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-316">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-316">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-317">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-317">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-318">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-318">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-319">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-319">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="ae395-320">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-320">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-321">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-321">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-322">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-322">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-323">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-323">SalesTransBuildNumberSample</span></span>

    ---

4. <span data-ttu-id="ae395-324">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="ae395-324">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-325">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-325">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-326">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-326">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-327">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-327">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="ae395-328">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-328">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="ae395-329">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="ae395-329">Rebuild the solution.</span></span>
6. <span data-ttu-id="ae395-330">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="ae395-330">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="ae395-331">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ae395-331">Cloud POS extension components</span></span>

1. <span data-ttu-id="ae395-332">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae395-332">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="ae395-333">**Pos.Extensions** プロジェクトで、既存のソース コードのフォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="ae395-333">Include the following existing source code folders in the **Pos.Extensions** project:</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-334">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-334">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="ae395-335">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-335">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-336">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-336">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-337">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-337">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-338">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="ae395-338">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="ae395-339">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-339">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-340">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-340">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="ae395-341">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-341">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-342">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-342">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-343">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-343">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-344">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-344">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-345">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-345">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="ae395-346">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-346">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-347">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-347">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-348">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-348">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-349">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-349">SalesTransBuildNumberSample</span></span>

    ---

    > [!NOTE]
    > <span data-ttu-id="ae395-350">プロジェクトに含まれているファイルだけでなく、プロジェクト フォルダーのすべてのファイルを表示するには、ソリューション エクスプ ローラーで**すべてのファイルを表示する** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae395-350">To view all files in the project folder, not just the files that are included in the project, select the **Show All Files** button in Solution Explorer.</span></span> <span data-ttu-id="ae395-351">このボタンを使用できない場合は、プロジェクトが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-351">If this button isn't available, make sure that you selected the project.</span></span> <span data-ttu-id="ae395-352">現時点でプロジェクトの一部ではないファイルとフォルダーのアイコンには点線があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-352">The icons of files and folders that aren't currently part of the project have a dotted outline.</span></span> <span data-ttu-id="ae395-353">プロジェクトに含めるためにフォルダーを右クリックし、**新しいプロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae395-353">Right-click the folder to include in the project, and then select **Include in Project**.</span></span>

3. <span data-ttu-id="ae395-354">**tsconfig.json** で除外リストから以下のフォルダーを削除して、コンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ae395-354">Enable the extensions to be compiled by removing the following folders from the exclude list in **tsconfig.json**:</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-355">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-355">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="ae395-356">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-356">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-357">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-357">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-358">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-358">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-359">RestrictingShiftDuration</span><span class="sxs-lookup"><span data-stu-id="ae395-359">RestrictingShiftDuration</span></span>
    - <span data-ttu-id="ae395-360">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-360">SalesTransBuildNumberSample</span></span>

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-361">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-361">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="ae395-362">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-362">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-363">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-363">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-364">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-364">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-365">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-365">SalesTransBuildNumberSample</span></span>

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-366">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-366">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="ae395-367">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-367">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="ae395-368">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="ae395-368">SequentialSignature</span></span>
    - <span data-ttu-id="ae395-369">AuditEventSignatureSample</span><span class="sxs-lookup"><span data-stu-id="ae395-369">AuditEventSignatureSample</span></span>
    - <span data-ttu-id="ae395-370">SalesTransBuildNumberSample</span><span class="sxs-lookup"><span data-stu-id="ae395-370">SalesTransBuildNumberSample</span></span>

    ---

4. <span data-ttu-id="ae395-371">**extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="ae395-371">Enable the extensions to be loaded by adding the following lines in **extensions.json**:</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-372">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-372">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-373">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-373">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

    # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-374">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-374">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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
    > <span data-ttu-id="ae395-375">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-375">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="ae395-376">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="ae395-376">Rebuild the solution.</span></span>
6. <span data-ttu-id="ae395-377">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ae395-377">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="ae395-378">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="ae395-378">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-retail-headquarters"></a><span data-ttu-id="ae395-379">小売用バックオフィスで要求されるパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="ae395-379">Set up required parameters in Retail headquarters</span></span>
<span data-ttu-id="ae395-380">詳細については、「[フランスのキャッシュ レジスター](./emea-fra-cash-registers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-380">For more information, see [Cash registers for France](./emea-fra-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="ae395-381">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="ae395-381">Production environment</span></span>

<span data-ttu-id="ae395-382">以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="ae395-382">Follow these steps to create deployable packages that contain Retail components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="ae395-383">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="ae395-383">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="ae395-384">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="ae395-384">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="ae395-385">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae395-385">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-386">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-386">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-387">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-387">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-388">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-388">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

        <span data-ttu-id="ae395-389">デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae395-389">To use a certificate that is stored in Azure Key Vault storage for digital signing, add the following line.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ae395-390">この明細行を追加する前に、このトピックの前の方にある[Azure Key Vault にデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-390">Before you add this line, complete the steps in the [Storing a certificate for digital signing in Azure Key Vault](#storing-a-certificate-for-digital-signing-in-azure-key-vault) section earlier in this topic.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DataSignatureKeyVaultSample" />
        ```

    2. <span data-ttu-id="ae395-391">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成**セクションに以下の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae395-391">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

3. <span data-ttu-id="ae395-392">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="ae395-392">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="ae395-393">**ItemGroup** セクションに次の行を追加して、配置可能なパッケージに Retail プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="ae395-393">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages.</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

    2. <span data-ttu-id="ae395-394">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="ae395-394">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="ae395-395">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-395">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

        # <a name="retail-735-and-latertabretail-7-3-5"></a>[<span data-ttu-id="ae395-396">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-396">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

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

        # <a name="retail-811-and-latertabretail-8-1-1"></a>[<span data-ttu-id="ae395-397">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="ae395-397">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

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

        <span data-ttu-id="ae395-398">デジタル署名に Azure Key Vault ストレージに格納されている証明書を使用するには、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae395-398">To use a certificate that is stored in Azure Key Vault storage for digital signing, add the following line.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ae395-399">この明細行を追加する前に、このトピックの前の方にある、[Azure Key Vaultにデジタル署名のための証明書を格納する](#storing-a-certificate-for-digital-signing-in-azure-key-vault) セクションにある手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-399">Before you add this line, complete the steps in the [Storing a certificate for digital signing in Azure Key Vault](#storing-a-certificate-for-digital-signing-in-azure-key-vault) section, earlier in this topic.</span></span>

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DataSignatureKeyVaultSample.dll" />
        ```

    3. <span data-ttu-id="ae395-400">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="ae395-400">Add the following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages.</span></span>

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

4. <span data-ttu-id="ae395-401">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="ae395-401">Update the Retail Server configuration file.</span></span> <span data-ttu-id="ae395-402">**RetailSDK\\Packages\\RetailServer\\Code\\ web.config**で、**extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae395-402">In **RetailSDK\\Packages\\RetailServer\\Code\\web.config**, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

5. <span data-ttu-id="ae395-403">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="ae395-403">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="ae395-404">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ae395-404">Then copy the configuration file to the **References** folder.</span></span> <span data-ttu-id="ae395-405">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="ae395-405">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>
6. <span data-ttu-id="ae395-406">ビルド番号、カテゴリ、および必要に応じて、コンプライアンスの証明書の番号を上書きします。</span><span class="sxs-lookup"><span data-stu-id="ae395-406">Override the build number and the category and number of the certificate of compliance, as required.</span></span> <span data-ttu-id="ae395-407">詳細については、このトピックの前の方にある、[レシートに印刷されるアプリケーション属性を指定する](#specifying-application-attributes-that-will-be-printed-on-receipts) セクションにある指示を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-407">For more information, see the instructions in the [Specifying application attributes that will be printed on receipts](#specifying-application-attributes-that-will-be-printed-on-receipts) section earlier in this topic.</span></span>
7. <span data-ttu-id="ae395-408">Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae395-408">Start the MSBuild Command Prompt for Visual Studio utility, and run **msbuild** under the Retail SDK folder to create deployable packages.</span></span>
8. <span data-ttu-id="ae395-409">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="ae395-409">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="ae395-410">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae395-410">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="ae395-411">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ae395-411">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="ae395-412">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae395-412">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="ae395-413">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="ae395-413">Sign in to POS.</span></span>
2. <span data-ttu-id="ae395-414">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae395-414">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="ae395-415">**ダウンロードの保留中**フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="ae395-415">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="ae395-416">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="ae395-416">Sign out of POS.</span></span>
4. <span data-ttu-id="ae395-417">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="ae395-417">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="ae395-418">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="ae395-418">Sign in to POS.</span></span>
6. <span data-ttu-id="ae395-419">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae395-419">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="ae395-420">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="ae395-420">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="ae395-421">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="ae395-421">Restart Modern POS.</span></span>
