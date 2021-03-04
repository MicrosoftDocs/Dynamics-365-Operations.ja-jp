---
title: ノルウェーのキャッシュ レジスタの配置ガイドライン
description: このトピックは、ノルウェーのローカライズ用配置ガイドです。
author: AlexChern0v
manager: olegkl
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Norway
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 5c08e88fe30d30ac25050294f08799368112b457
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985941"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a><span data-ttu-id="0e99e-103">ノルウェーのキャッシュ レジスタの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="0e99e-103">Deployment guidelines for cash registers for Norway</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e99e-104">このトピックは、Dynamics 365 Commerce のノルウェーでのローカライズを有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="0e99e-104">This topic is a deployment guide that shows how to enable the Dynamics 365 Commerce localization for Norway.</span></span> <span data-ttu-id="0e99e-105">ローカライズは、コマース コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-105">The localization consists of several extensions of Commerce components.</span></span> <span data-ttu-id="0e99e-106">たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引を登録、デジタル署名販売取引、およびローカルの形式で X および Z レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-106">For example, the extensions let you print custom fields on receipts, register additional audit events, sales transactions, and payment transactions in Point of Sale (POS), digitally sign sales transactions, and print X and Z reports in local formats.</span></span> <span data-ttu-id="0e99e-107">ノルウェーのローカライズの詳細については、 [ノルウェーのキャッシュ レジスター機能](./emea-nor-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-107">For more information about the localization for Norway, see [Cash register functionality for Norway](./emea-nor-cash-registers.md).</span></span>

<span data-ttu-id="0e99e-108">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="0e99e-108">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="0e99e-109">SDK に関する詳細については、[Retail ソフトウエア開発キット (SDK) アーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-109">For information about the SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="0e99e-110">このサンプルは Commerce runtime (CRT)、Retail Server、そして POS の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-110">This sample consists of extensions for the Commerce runtime (CRT), Retail Server, and POS.</span></span> <span data-ttu-id="0e99e-111">このサンプルを実行するには、CRT、Retail Servers および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-111">To run this sample, you must modify and build the CRT, Retail Server, and POS projects.</span></span> <span data-ttu-id="0e99e-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="0e99e-113">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="0e99e-114">Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-114">In Commerce 10.0.8 and above, Retail Server is known as Commerce Scale Unit.</span></span> <span data-ttu-id="0e99e-115">このトピックは、アプリの以前の複数のバージョンに適用されるため、このトピック全体で *Retail サーバー* を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-115">Because this topic applies to multiple previous versions of the app, *Retail Server* is used throughout the topic.</span></span>

> [!NOTE]
> <span data-ttu-id="0e99e-116">使用しているコマースのバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-116">Some steps in the procedures in this topic differ, depending on the version of Commerce that you're using.</span></span> <span data-ttu-id="0e99e-117">詳細については、 [Dynamics 365 Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-117">For more information, see [What's new or changed in Dynamics 365 Retail](../get-started/whats-new.md).</span></span>

### <a name="using-certificate-profiles-in-commerce-channels"></a><span data-ttu-id="0e99e-118">Commerce チャネルでの証明書プロファイルの使用</span><span class="sxs-lookup"><span data-stu-id="0e99e-118">Using certificate profiles in Commerce channels</span></span>

<span data-ttu-id="0e99e-119">Commerce バージョン 10.0.15 では、Key Vault または本社が使用できない場合に、オフラインにするためのフェールオーバーをサポートする[小売店舗のユーザー定義の証明書プロファイル](./certificate-profiles-for-retail-stores.md) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-119">In Commerce versions 10.0.15 and later, you can use the [User-defined certificate profiles for retail stores](./certificate-profiles-for-retail-stores.md) feature that supports failover to offline when Key Vault or Commerce headquarters aren't available.</span></span> <span data-ttu-id="0e99e-120">この機能は、[小売チャンネルのシークレットを管理 ](../dev-itpro/manage-secrets.md) を拡張ます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-120">The feature extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature.</span></span>

<span data-ttu-id="0e99e-121">CRT でこの機能を適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-121">To apply this functionality in the CRT extension, follow these steps.</span></span>

1. <span data-ttu-id="0e99e-122">新しい CRT 拡張機能プロジェクトを作成します (C# クラス ライブラリ プロジェクト タイプ)。</span><span class="sxs-lookup"><span data-stu-id="0e99e-122">Create a new CRT extension project (C# class library project type).</span></span> <span data-ttu-id="0e99e-123">Retail ソフトウェア開発キット (SDK) からサンプル テンプレートを使用します (RetailSDK\SampleExtensions\CommerceRuntime)。</span><span class="sxs-lookup"><span data-stu-id="0e99e-123">Use the sample templates from the Retail software development kit (SDK) (RetailSDK\SampleExtensions\CommerceRuntime).</span></span>

2. <span data-ttu-id="0e99e-124">CertificateSignatureServiceRequest のカスタム ハンドラーを SequentialSignatureRegister プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-124">Add custom handler for CertificateSignatureServiceRequest in the SequentialSignatureRegister project.</span></span>

3. <span data-ttu-id="0e99e-125">シークレット呼び出しを読み取るには、プロファイスされたパラメータのあるコンストラクターを使用し、GetUserDefinedSecretCertificateServiceRequest を実行します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-125">To read a secret call, GetUserDefinedSecretCertificateServiceRequest using a constructor with profileId parameter.</span></span> <span data-ttu-id="0e99e-126">これにより、証明書プロファイルの設定で機能が開始されます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-126">That will start the functionality working with settings from Certificate profiles.</span></span> <span data-ttu-id="0e99e-127">この設定に基づいて、証明書は Azure Key Vault またはローカルマシン ストレージから取得されます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-127">Based on the settings, the certificate will be retrieved either from Azure Key Vault or local machine storage.</span></span>
    
    <span data-ttu-id="0e99e-128">GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);  GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);</span><span class="sxs-lookup"><span data-stu-id="0e99e-128">GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);  GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);</span></span>
    
    <span data-ttu-id="0e99e-129">X509Certificate2 証明書 = getUserDefinedSecretCertificateServiceResponse.Certificate;</span><span class="sxs-lookup"><span data-stu-id="0e99e-129">X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;</span></span>
    
4. <span data-ttu-id="0e99e-130">証明書が取得されたら、データ署名に進みます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-130">When the certificate is retrieved, proceed with data signing.</span></span>

5. <span data-ttu-id="0e99e-131">CRT 拡張機能プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-131">Build the CRT extension project.</span></span>

6. <span data-ttu-id="0e99e-132">出力クラス ライブラリをコピーし、手動テスト用の ...\RetailServer\webroot\bin\Ext に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-132">Copy the output class library and paste it into ...\RetailServer\webroot\bin\Ext for manual testing.</span></span>

7. <span data-ttu-id="0e99e-133">CommerceRuntime.Ext.config ファイルで、カスタム ライブラリ情報で拡張機能の合成セクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-133">In the CommerceRuntime.Ext.config file, update the extension composition section with the custom library information.</span></span>

## <a name="development-environment"></a><span data-ttu-id="0e99e-134">開発環境</span><span class="sxs-lookup"><span data-stu-id="0e99e-134">Development environment</span></span>

<span data-ttu-id="0e99e-135">サンプルをテストして拡張できるように開発環境を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-135">Complete these procedures to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="0e99e-136">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-136">The CRT extension components</span></span>

<span data-ttu-id="0e99e-137">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-137">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="0e99e-138">次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-138">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="receiptsnorway-component"></a><span data-ttu-id="0e99e-139">ReceiptsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-139">ReceiptsNorway component</span></span>

1. <span data-ttu-id="0e99e-140">**Runtime.Extensions.ReceiptsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-140">Find the **Runtime.Extensions.ReceiptsNorway** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-141">**Extensions.ReceiptsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.ReceiptsNorway.dll** アセンブリファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-141">In the **Extensions.ReceiptsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.ReceiptsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-142">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-142">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-143">**Retail Server:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Retail Serverのサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-143">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-144">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-144">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-145">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-145">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-146">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-146">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-147">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-147">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-148">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-148">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-149">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-149">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-150">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-150">These files aren't intended for any customizations.</span></span>

#### <a name="salespaymenttransext-component"></a><span data-ttu-id="0e99e-151">SalesPaymentTransExt コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-151">SalesPaymentTransExt component</span></span>

1. <span data-ttu-id="0e99e-152">**Runtime.Extensions.SalesPaymentTransExt** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-152">Find the **Runtime.Extensions.SalesPaymentTransExt** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-153">**Extensions.SalesPaymentTransExt\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-153">In the **Extensions.SalesPaymentTransExt\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-154">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-154">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-155">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-155">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-156">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-156">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-157">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-157">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-158">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-158">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-159">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-159">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-160">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-160">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-161">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-161">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-162">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-162">These files aren't intended for any customizations.</span></span>

#### <a name="xzreportsnorway-component"></a><span data-ttu-id="0e99e-163">XZReportsNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-163">XZReportsNorway component</span></span>

1. <span data-ttu-id="0e99e-164">**Runtime.Extensions.XZReportsNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-164">Find the **Runtime.Extensions.XZReportsNorway** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-165">**Extensions.XZReportsNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.XZReportsNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-165">In the **Extensions.XZReportsNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.XZReportsNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-166">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-166">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-167">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-167">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-168">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-168">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-169">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-169">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-170">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-170">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-171">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-171">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-172">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-172">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-173">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-173">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-174">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-174">These files aren't intended for any customizations.</span></span>

# <a name="application-update-4"></a>[<span data-ttu-id="0e99e-175">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-175">Application update 4</span></span>](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="0e99e-176">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-176">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="0e99e-177">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-177">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-178">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-178">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-179">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-179">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-180">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-180">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-181">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-181">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-182">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-182">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-183">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-183">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-184">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-184">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-185">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-185">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-186">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-186">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-187">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-187">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="0e99e-188">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-188">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="0e99e-189">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-189">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="0e99e-190">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-190">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="0e99e-191">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-191">Build the project.</span></span>
4. <span data-ttu-id="0e99e-192">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-192">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="0e99e-193">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-193">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="0e99e-194">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-194">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="0e99e-195">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-195">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-196">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-196">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-197">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-197">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="0e99e-198">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-198">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-199">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-199">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-200">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-200">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="0e99e-201">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-201">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-202">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-202">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-203">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-203">These files aren't intended for any customizations.</span></span>

# <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-204">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-204">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="0e99e-205">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-205">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="0e99e-206">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-206">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-207">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-207">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-208">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-208">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-209">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-209">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-210">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-210">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-211">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-211">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-212">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-212">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-213">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-213">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-214">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-214">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-215">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-215">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-216">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-216">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="0e99e-217">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-217">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="0e99e-218">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-218">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="0e99e-219">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-219">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="0e99e-220">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-220">Build the project.</span></span>
4. <span data-ttu-id="0e99e-221">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-221">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="0e99e-222">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-222">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="0e99e-223">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-223">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="0e99e-224">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-224">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-225">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-225">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-226">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-226">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="0e99e-227">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-227">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-228">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-228">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-229">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-229">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="0e99e-230">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-230">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-231">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-231">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-232">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-232">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturesamplemessages-component"></a><span data-ttu-id="0e99e-233">SalesTransactionSignatureSample.Messages コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-233">SalesTransactionSignatureSample.Messages component</span></span>

1. <span data-ttu-id="0e99e-234">**Runtime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-234">Find the **Runtime.Extensions.SalesTransactionSignatureSample.Messages** project.</span></span>
2. <span data-ttu-id="0e99e-235">**Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-235">In the **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-236">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-236">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-237">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-237">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-238">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-238">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-239">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-239">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-240">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-240">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-241">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-241">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-242">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-242">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-243">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-243">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-244">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-244">These files aren't intended for any customizations.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="0e99e-245">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-245">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="0e99e-246">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-246">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="0e99e-247">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-247">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-248">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-248">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-249">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-249">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-250">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-250">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-251">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-251">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-252">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-252">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-253">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-253">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-254">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-254">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-255">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-255">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-256">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-256">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-257">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-257">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignature-sample-component"></a><span data-ttu-id="0e99e-258">SalesTransactionSignature サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-258">SalesTransactionSignature sample component</span></span>

1. <span data-ttu-id="0e99e-259">**Runtime.Extensions.SalesTransactionSignatureSample** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-259">Find the **Runtime.Extensions.SalesTransactionSignatureSample** project.</span></span>
2. <span data-ttu-id="0e99e-260">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-260">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="0e99e-261">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-261">Build the project.</span></span>
4. <span data-ttu-id="0e99e-262">**Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-262">In the **Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="0e99e-263">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-263">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
    - <span data-ttu-id="0e99e-264">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-264">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

5. <span data-ttu-id="0e99e-265">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-265">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-266">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-266">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-267">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-267">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="0e99e-268">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-268">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-269">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-269">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-270">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-270">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="0e99e-271">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-271">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-272">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-272">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-273">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-273">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="0e99e-274">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-274">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="0e99e-275">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-275">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="0e99e-276">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-276">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-277">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-277">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-278">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-278">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-279">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-279">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-280">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-280">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a><span data-ttu-id="0e99e-281">RegisterAuditEvent サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-281">RegisterAuditEvent sample component</span></span>

1. <span data-ttu-id="0e99e-282">**Runtime.Extensions.RegisterAuditEventSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-282">Find the **Runtime.Extensions.RegisterAuditEventSample** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-283">**Extensions.RegisterAuditEventSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-283">In the **Extensions.RegisterAuditEventSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-284">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-284">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-285">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-285">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-286">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-286">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-287">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-287">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-288">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-288">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-289">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-289">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-290">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-290">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-291">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-291">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-292">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-292">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="0e99e-293">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-293">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="0e99e-294">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-294">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="0e99e-295">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-295">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="0e99e-296">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-296">Build the project.</span></span>
4. <span data-ttu-id="0e99e-297">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-297">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="0e99e-298">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-298">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="0e99e-299">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-299">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="0e99e-300">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-300">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-301">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-301">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-302">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-302">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="0e99e-303">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-303">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-304">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-304">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-305">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-305">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="0e99e-306">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-306">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-307">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-307">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-308">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-308">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="0e99e-309">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-309">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="0e99e-310">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-310">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="0e99e-311">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-311">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-312">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-312">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-313">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-313">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-314">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-314">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-315">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-315">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-316">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-316">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-317">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-317">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-318">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-318">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-319">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-319">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-320">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-320">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="0e99e-321">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-321">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="0e99e-322">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-322">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="0e99e-323">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-323">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-324">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-324">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-325">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-325">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-326">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-326">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="0e99e-327">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-327">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="0e99e-328">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-328">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-329">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-329">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-330">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-330">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-331">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-331">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-332">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-332">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-333">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-333">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-334">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-334">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-335">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-335">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-336">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-336">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-337">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-337">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-338">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-338">These files aren't intended for any customizations.</span></span>

# <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-339">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-339">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a><span data-ttu-id="0e99e-340">RegisterAuditEvent ノルウェイ コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-340">RegisterAuditEventNorway component</span></span>

1. <span data-ttu-id="0e99e-341">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-341">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-342">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-342">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-343">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-343">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="0e99e-344">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-344">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-345">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-345">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-346">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-346">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="0e99e-347">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-347">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="0e99e-348">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-348">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="0e99e-349">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-349">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="0e99e-350">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-350">Build the project.</span></span>
4. <span data-ttu-id="0e99e-351">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-351">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="0e99e-352">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-352">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="0e99e-353">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-353">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="0e99e-354">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-354">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-355">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-355">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-356">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-356">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="0e99e-357">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-357">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-358">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-358">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-359">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-359">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="0e99e-360">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-360">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-361">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-361">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-362">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-362">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="0e99e-363">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-363">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="0e99e-364">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-364">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="0e99e-365">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-365">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-366">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-366">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-367">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-367">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-368">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-368">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-369">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-369">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-370">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-370">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-371">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-371">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-372">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-372">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-373">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-373">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-374">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-374">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="0e99e-375">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-375">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="0e99e-376">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-376">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="0e99e-377">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-377">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-378">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-378">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-379">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-379">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-380">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-380">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="0e99e-381">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-381">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="0e99e-382">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-382">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-383">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-383">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-384">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-384">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-385">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-385">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-386">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-386">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-387">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-387">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-388">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-388">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-389">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-389">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-390">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-390">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-391">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-391">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-392">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-392">These files aren't intended for any customizations.</span></span>

# <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-393">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-393">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a><span data-ttu-id="0e99e-394">RegisterAuditEvent ノルウェイ コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-394">RegisterAuditEventNorway component</span></span>

1. <span data-ttu-id="0e99e-395">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-395">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-396">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-396">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-397">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-397">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="0e99e-398">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-398">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-399">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-399">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-400">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-400">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregister-component"></a><span data-ttu-id="0e99e-401">SequentialSignatureRegister コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-401">SequentialSignatureRegister component</span></span>

1. <span data-ttu-id="0e99e-402">**Runtime.Extensions.SequentialSignatureRegister** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-402">Find the **Runtime.Extensions.SequentialSignatureRegister** project.</span></span>
2. <span data-ttu-id="0e99e-403">拇印を指定することで **App.config** ファイルを変更し、場所を格納し、また署名販売取引に使用される証明書の名前を格納します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-403">Modify the **App.config** file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span>
3. <span data-ttu-id="0e99e-404">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-404">Build the project.</span></span>
4. <span data-ttu-id="0e99e-405">**Extensions.SequentialSignatureRegister\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-405">In the **Extensions.SequentialSignatureRegister\\bin\\Debug** folder, find the following files:</span></span>

    - <span data-ttu-id="0e99e-406">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-406">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** assembly file</span></span>
    - <span data-ttu-id="0e99e-407">**Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-407">The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** configuration file</span></span>

5. <span data-ttu-id="0e99e-408">ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-408">Copy the files to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-409">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-409">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-410">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-410">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

6. <span data-ttu-id="0e99e-411">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-411">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-412">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-412">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-413">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-413">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

7. <span data-ttu-id="0e99e-414">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-414">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-415">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-415">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-416">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-416">These files aren't intended for any customizations.</span></span>

#### <a name="salestransactionsignaturenorway-component"></a><span data-ttu-id="0e99e-417">SalesTransactionSignatureNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-417">SalesTransactionSignatureNorway component</span></span>

1. <span data-ttu-id="0e99e-418">**Runtime.Extensions.SalesTransactionSignatureNorway** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-418">Find the **Runtime.Extensions.SalesTransactionSignatureNorway** project.</span></span>
2. <span data-ttu-id="0e99e-419">**Extensions.SalesTransactionSignatureNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-419">In the **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-420">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-420">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-421">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-421">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-422">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-422">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-423">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-423">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-424">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-424">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-425">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-425">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-426">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-426">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-427">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-427">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-428">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-428">These files aren't intended for any customizations.</span></span>

#### <a name="sequentialsignatureregistercontracts-component"></a><span data-ttu-id="0e99e-429">SequentialSignatureRegister.Contracts コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-429">SequentialSignatureRegister.Contracts component</span></span>

1. <span data-ttu-id="0e99e-430">**Runtime.Extensions.SequentialSignatureRegister.Contracts** プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-430">Find the **Runtime.Extensions.SequentialSignatureRegister.Contracts** project.</span></span>
2. <span data-ttu-id="0e99e-431">**Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-431">In the **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-432">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-432">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-433">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-433">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-434">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-434">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

#### <a name="salespaymenttransextnorway-component"></a><span data-ttu-id="0e99e-435">SalesPaymentTransExtNorway コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-435">SalesPaymentTransExtNorway component</span></span>

1. <span data-ttu-id="0e99e-436">**Runtime.Extensions.SalesPaymentTransExtNorway** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-436">Find the **Runtime.Extensions.SalesPaymentTransExtNorway** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-437">**Extensions.SalesPaymentTransExtNorway\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-437">In the **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-438">アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-438">Copy the assembly file to the CRT extensions folder:</span></span>

    - <span data-ttu-id="0e99e-439">**Retail Server:** アセンブリを IIS Retail Server サイトがある場所の下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-439">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-440">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-440">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="0e99e-441">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-441">Find the extension configuration file for CRT:</span></span>

    - <span data-ttu-id="0e99e-442">**Retail Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-442">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail Server site location.</span></span>
    - <span data-ttu-id="0e99e-443">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-443">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="0e99e-444">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-444">Register the CRT change in the extension configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > <span data-ttu-id="0e99e-445">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="0e99e-445">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="0e99e-446">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-446">These files aren't intended for any customizations.</span></span>

---

### <a name="the-retail-server-extension-components"></a><span data-ttu-id="0e99e-447">Retail Server 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-447">The Retail Server extension components</span></span>

#### <a name="salestransactionsignature-retail-server-sample-component"></a><span data-ttu-id="0e99e-448">SalesTransactionSignature Retail Server サンプル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-448">SalesTransactionSignature Retail Server sample component</span></span>

1. <span data-ttu-id="0e99e-449">**RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-449">In the **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-450">**RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.RetailServer.SalesTransactionSignatureSample.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-450">In the **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.RetailServer.SalesTransactionSignatureSample.dll** assembly file.</span></span>
3. <span data-ttu-id="0e99e-451">アセンブリ ファイルを Retail Server 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-451">Copy the assembly file to the Retail Server extensions folder.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-452">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-452">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="0e99e-453">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="0e99e-453">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-454">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-454">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="0e99e-455">フォルダーは、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="0e99e-455">The folder is the **\\bin** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-456">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-456">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="0e99e-457">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="0e99e-457">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-458">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-458">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="0e99e-459">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="0e99e-459">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-460">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-460">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="0e99e-461">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="0e99e-461">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-462">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-462">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="0e99e-463">フォルダーは、 IIS Retail Server サイトがある場所の下の **\\bin\\ext** フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="0e99e-463">The folder is the **\\bin\\ext** folder under the IIS Retail Server site location.</span></span>

    ---

4. <span data-ttu-id="0e99e-464">Retail Server のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-464">Find the configuration file for Retail Server.</span></span> <span data-ttu-id="0e99e-465">ファイル名は **web.config** で、IIS Retail Server サイトがある場所の下のルート フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-465">The file is named **web.config**, and it's in the root folder under the IIS Retail Server site location.</span></span>
5. <span data-ttu-id="0e99e-466">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-466">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. <span data-ttu-id="0e99e-467">Retail Server 拡張機能の依存関係を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-467">Register the dependencies of the Retail Server extensions.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-468">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-468">Application update 4</span></span>](#tab/app-update-4/)

    1. <span data-ttu-id="0e99e-469">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-469">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the following files:</span></span>

        - <span data-ttu-id="0e99e-470">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** アセンブリ ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-470">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** assembly file</span></span>
        - <span data-ttu-id="0e99e-471">**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** コンフィギュレーション ファイル</span><span class="sxs-lookup"><span data-stu-id="0e99e-471">The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** configuration file</span></span>

    2. <span data-ttu-id="0e99e-472">ファイルを、IIS Retail Server サイトがある場所の下の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-472">Copy the files to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="0e99e-473">CRT 用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-473">Register the CRT change in the extension configuration file for CRT.</span></span> <span data-ttu-id="0e99e-474">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-474">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-475">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-475">Application update 5 and later</span></span>](#tab/app-update-5-and-later/)

    1. <span data-ttu-id="0e99e-476">**CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-476">In the **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** assembly file.</span></span>
    2. <span data-ttu-id="0e99e-477">ファイルをIIS Retail Server サイトがある場所の **\\bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-477">Copy the file to the **\\bin** folder under the IIS Retail Server site location.</span></span>
    3. <span data-ttu-id="0e99e-478">CRT 用拡張機能コンフィギュレーションファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-478">Register the CRT change in the extension configuration file for CRT.</span></span> <span data-ttu-id="0e99e-479">ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-479">This file is named **commerceruntime.ext.config**, and it's in the **bin** folder under the IIS Retail Server site location.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-480">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-480">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-481">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="0e99e-481">No actions are required.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-482">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-482">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="0e99e-483">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="0e99e-483">No actions are required.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-484">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-484">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="0e99e-485">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="0e99e-485">No actions are required.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-486">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-486">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-487">作業は不要です。</span><span class="sxs-lookup"><span data-stu-id="0e99e-487">No actions are required.</span></span>

    ---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="0e99e-488">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-488">The Modern POS extension components</span></span>

#### <a name="implement-the-proxy-code-for-offline-mode"></a><span data-ttu-id="0e99e-489">オフライン モード用プロキシ コードを実装します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-489">Implement the proxy code for offline mode</span></span>

<span data-ttu-id="0e99e-490">この箇所は Retail Server コントローラーと同じですが、クライアントが接続されていない場合に使用されるローカル CRT を拡張します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-490">This part is equivalent to the Retail Server controller, but it extends the local CRT that is used when the client isn't connected.</span></span>

1. <span data-ttu-id="0e99e-491">**Customization.settings** ファイルで、**@(RetailServerLibraryPathForProxyGeneration)** セクションを変更し、プロキシ生成で新しい Retail Server アセンブリを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-491">In the **customization.settings** file, change the **@(RetailServerLibraryPathForProxyGeneration)** section so that it uses the new Retail Server assembly for proxy generation.</span></span>
2. <span data-ttu-id="0e99e-492">**StoreOperationsManager** クラスで次のインターフェイス メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-492">Implement the following interface methods in the **StoreOperationsManager** class.</span></span> <span data-ttu-id="0e99e-493">最初の繰り返しには、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-493">For the first iteration, add the following code:</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-494">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-494">Application update 4</span></span>](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-495">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-495">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-496">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-496">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-497">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-497">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-498">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-498">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="0e99e-499">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-499">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-500">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-500">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="0e99e-501">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-501">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-502">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-502">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-503">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-503">This step doesn't apply to this version.</span></span>

    ---

3. <span data-ttu-id="0e99e-504">プロキシ コードを再生成するには、コマンドラインから **msbuild/t:Rebuild** コマンドを使用して **プロキシ** フォルダーを構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-504">To regenerate the proxy code, build the **Proxies** folder from the command line by using the **msbuild /t:Rebuild** command.</span></span>
4. <span data-ttu-id="0e99e-505">**Proxies.RetailProxy** プロジェクトの依存関係を解決します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-505">Resolve the **Proxies.RetailProxy** project dependencies:</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-506">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-506">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="0e99e-507">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** project to reference **SalesTransactionSignatureSample** に追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-507">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample**.</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-508">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-508">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="0e99e-509">**RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** を開き、**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** プロジェクトをソリューションに追加し、プロジェクト参照を **RetailProxy** プロジェクトと、**SalesTransactionSignatureSample.Messages** 参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-509">Open **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, add the **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** project to the solution, and add a project reference to the **RetailProxy** project to reference **SalesTransactionSignatureSample.Messages**.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-510">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-510">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-511">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-511">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-512">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-512">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="0e99e-513">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-513">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-514">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-514">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="0e99e-515">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-515">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-516">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-516">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-517">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-517">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="0e99e-518">**StoreOperationsManager** クラスでインターフェイス メソッドを調節します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-518">Adjust the interface methods in the **StoreOperationsManager** class:</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-519">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-519">Application update 4</span></span>](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-520">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-520">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-521">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-521">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-522">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-522">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-523">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-523">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="0e99e-524">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-524">This step doesn't apply to this version.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-525">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-525">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    > [!NOTE]
    > <span data-ttu-id="0e99e-526">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-526">This step doesn't apply to this version.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-527">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-527">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    > [!NOTE]
    > <span data-ttu-id="0e99e-528">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e99e-528">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="0e99e-529">**dllhost.exe.config** ファイルを更新し、クライアント ブローカーが新しい RetailProxy アセンブリを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-529">Update the **dllhost.exe.config** file so that the client broker loads the new RetailProxy assembly.</span></span>

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a><span data-ttu-id="0e99e-530">小売プロキシ拡張コンポーネント (Retail 7.3.1 およびそれ以降)</span><span class="sxs-lookup"><span data-stu-id="0e99e-530">Retail proxy extension component (Retail 7.3.1 and later)</span></span>

<span data-ttu-id="0e99e-531">Retail 7.3.1 もしくはそれ以降を使用しているときに限り、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-531">Complete the following procedure only if you're using Retail 7.3.1 and later.</span></span>

1. <span data-ttu-id="0e99e-532">**RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample**  フォルダーで、**RetailServer.Extensions.SalesTransactionSignatureSample** プロジェクトを検索し、構築します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-532">In the **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** folder, find the **RetailServer.Extensions.SalesTransactionSignatureSample** project, and build it.</span></span>
2. <span data-ttu-id="0e99e-533">**RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** アセンブリ ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-533">In the **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** folder, find the **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** assembly file.</span></span>
3. <span data-ttu-id="0e99e-534">アセンブリ ファイルをローカル CRT クライアント ブローカーの下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-534">Copy the assembly files to the **\\ext** folder under the local CRT client broker location.</span></span>
4. <span data-ttu-id="0e99e-535">拡張機能コンフィギュレーション ファイルで Retail プロキシの変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-535">Register the Retail proxy change in the extension configuration file.</span></span> <span data-ttu-id="0e99e-536">ファイル名は **RetailProxy.MPOSOffline.ext.config** で、ローカル CRT クライアント ブローカーの場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-536">The file is named **RetailProxy.MPOSOffline.ext.config**, and it's under the local CRT client broker location.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a><span data-ttu-id="0e99e-537">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-537">Modern POS extension components</span></span>

1. <span data-ttu-id="0e99e-538">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-538">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="0e99e-539">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-539">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0e99e-540">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-540">Modern POS must not be customized.</span></span> <span data-ttu-id="0e99e-541">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-541">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="0e99e-542">**Pos.Extensions** プロジェクトが、次の既存のソース コード フォルダーを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-542">Include the following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-543">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-543">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="0e99e-544">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-544">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-545">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-545">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-546">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-546">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="0e99e-547">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-547">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-548">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-548">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-549">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-549">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="0e99e-550">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-550">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-551">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-551">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-552">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-552">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="0e99e-553">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-553">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-554">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-554">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-555">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-555">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-556">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-556">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-557">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-557">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="0e99e-558">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-558">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-559">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-559">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-560">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-560">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-561">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-561">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="0e99e-562">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-562">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-563">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-563">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-564">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-564">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="0e99e-565">除外リストから次のフォルダーを削除して、**tsconfig.json** で拡張機能がコンパイルされるようにします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-565">Enable the extensions to be compiled in **tsconfig.json** by removing the following folders from the exclude list.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-566">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-566">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="0e99e-567">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-567">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-568">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-568">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-569">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-569">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="0e99e-570">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-570">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-571">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-571">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-572">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-572">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="0e99e-573">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-573">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-574">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-574">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-575">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-575">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="0e99e-576">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-576">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-577">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-577">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-578">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-578">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-579">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-579">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-580">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-580">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="0e99e-581">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-581">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-582">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-582">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-583">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-583">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-584">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-584">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="0e99e-585">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-585">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-586">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-586">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-587">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-587">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="0e99e-588">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-588">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-589">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-589">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-590">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-590">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-591">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-591">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-592">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-592">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-593">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-593">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-594">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-594">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > <span data-ttu-id="0e99e-595">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-595">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="0e99e-596">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-596">Rebuild the solution.</span></span>
6. <span data-ttu-id="0e99e-597">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-597">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="0e99e-598">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0e99e-598">Cloud POS extension components</span></span>

1. <span data-ttu-id="0e99e-599">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-599">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="0e99e-600">**Pos.Extensions** プロジェクトの、既存ソース コード フォルダーを含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-600">Include following existing source code folders in the **Pos.Extensions** project.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-601">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-601">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="0e99e-602">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-602">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-603">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-603">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-604">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-604">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="0e99e-605">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-605">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-606">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-606">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-607">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-607">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="0e99e-608">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-608">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-609">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-609">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-610">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-610">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="0e99e-611">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-611">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-612">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-612">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-613">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-613">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-614">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-614">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-615">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-615">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="0e99e-616">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-616">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-617">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-617">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-618">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-618">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-619">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-619">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="0e99e-620">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-620">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-621">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-621">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-622">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-622">SequentialSignature</span></span>

    ---

3. <span data-ttu-id="0e99e-623">除外リストから次のフォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-623">Enable the extensions to be compiled in **tsconfig.json** by removing following folders from the exclude list.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-624">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-624">Application update 4</span></span>](#tab/app-update-4)

    - <span data-ttu-id="0e99e-625">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-625">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-626">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-626">SalesTransactionSignatureSample</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-627">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-627">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    - <span data-ttu-id="0e99e-628">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-628">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-629">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-629">SalesTransactionSignatureSample</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-630">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-630">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="0e99e-631">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-631">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-632">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-632">SalesTransactionSignatureSample</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-633">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-633">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="0e99e-634">AuditEventExtensionSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-634">AuditEventExtensionSample</span></span>
    - <span data-ttu-id="0e99e-635">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-635">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-636">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-636">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-637">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-637">SequentialSignature</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-638">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-638">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    - <span data-ttu-id="0e99e-639">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-639">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-640">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-640">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-641">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-641">SequentialSignature</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-642">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-642">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    - <span data-ttu-id="0e99e-643">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="0e99e-643">SalesTransactionSignatureSample</span></span>
    - <span data-ttu-id="0e99e-644">SalesTransactionSignatureNorway</span><span class="sxs-lookup"><span data-stu-id="0e99e-644">SalesTransactionSignatureNorway</span></span>
    - <span data-ttu-id="0e99e-645">SequentialSignature</span><span class="sxs-lookup"><span data-stu-id="0e99e-645">SequentialSignature</span></span>

    ---

4. <span data-ttu-id="0e99e-646">適切な場所に次の行を追加して、**extensions.json** で拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-646">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate place.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-647">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-647">Application update 4</span></span>](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-648">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-648">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-649">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-649">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-650">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-650">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-651">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-651">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-652">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-652">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > <span data-ttu-id="0e99e-653">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-653">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.</span></span>

5. <span data-ttu-id="0e99e-654">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-654">Rebuild the solution.</span></span>
6. <span data-ttu-id="0e99e-655">**実行** コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-655">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
7. <span data-ttu-id="0e99e-656">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-656">Test the functionality.</span></span>

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="0e99e-657">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="0e99e-657">Set up required parameters in Headquarters</span></span>

<span data-ttu-id="0e99e-658">詳細については、 [ノルウェイのキャッシュ レジスター機能](./emea-nor-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-658">For more information, see [Cash register functionality for Norway](./emea-nor-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="0e99e-659">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="0e99e-659">Production environment</span></span>

<span data-ttu-id="0e99e-660">以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-660">Follow these steps to create deployable packages that contain Commerce components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="0e99e-661">[クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-661">Complete the steps in the [Cloud POS extension components](#cloud-pos-extension-components) or [Modern POS extension components](#modern-pos-extension-components) section earlier in this topic.</span></span>
2. <span data-ttu-id="0e99e-662">**RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-662">Make the following changes in the package configuration files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="0e99e-663">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの **構成** セクションに、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-663">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files, add the following lines to the **composition** section:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-664">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-664">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-665">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-665">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="0e99e-666">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-666">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-667">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-667">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-668">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-668">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-669">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-669">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. <span data-ttu-id="0e99e-670">コマース プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-670">Enable Commerce Proxy customization:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-671">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-671">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="0e99e-672">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-672">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-673">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-673">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="0e99e-674">**dllhost.exe.config** コンフィギュレーション ファイルで、**コンフィギュレーション** セクションの **appSettings** サブセクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-674">In the **dllhost.exe.config** configuration file, add the following lines to the **appSettings** subsection of the **configuration** section.</span></span>

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="0e99e-675">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-675">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="0e99e-676">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-676">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-677">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-677">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="0e99e-678">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-678">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-679">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-679">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="0e99e-680">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-680">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-681">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-681">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="0e99e-682">**RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、**構成** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-682">In the **RetailProxy.MPOSOffline.ext.config** configuration file, add the following lines to the **composition** section:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. <span data-ttu-id="0e99e-683">**Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-683">Make the following changes in the **Customization.settings** package customization configuration file:</span></span>

    1. <span data-ttu-id="0e99e-684">小売プロキシ カスタマイズを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-684">Enable Retail Proxy customization.</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-685">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-685">Application update 4</span></span>](#tab/app-update-4)

        <span data-ttu-id="0e99e-686">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-686">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-687">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-687">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        <span data-ttu-id="0e99e-688">**&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-688">Add the following lines to the **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** section.</span></span>

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="0e99e-689">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-689">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="0e99e-690">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-690">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-691">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-691">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        <span data-ttu-id="0e99e-692">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-692">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-693">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-693">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        <span data-ttu-id="0e99e-694">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-694">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-695">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-695">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        <span data-ttu-id="0e99e-696">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに小売プロキシ拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-696">Add the following lines to the **ItemGroup** section to include the Retail proxy extension in the deployable packages:</span></span>

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. <span data-ttu-id="0e99e-697">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-697">Add the following lines to the **ItemGroup** section to include the CRT extensions in the deployable packages:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-698">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-698">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-699">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-699">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="0e99e-700">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-700">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-701">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-701">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-702">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-702">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-703">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-703">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. <span data-ttu-id="0e99e-704">**ItemGroup** セクションに次の行を追加し、配置可能なパッケージに Retail Server 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-704">Add following lines to the **ItemGroup** section to include the Retail Server extension in the deployable packages:</span></span>

        # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-705">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-705">Application update 4</span></span>](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-706">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-706">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[<span data-ttu-id="0e99e-707">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-707">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-708">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-708">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-709">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-709">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-710">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-710">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. <span data-ttu-id="0e99e-711">以下のファイルを修正して、配置可能なパッケージ内に ノルウェーのリソース ファイルを含めます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-711">Modify the following files to include the resource files for Norway in deployable packages:</span></span>
    - <span data-ttu-id="0e99e-712">Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj</span><span class="sxs-lookup"><span data-stu-id="0e99e-712">Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj</span></span>
    - <span data-ttu-id="0e99e-713">Packages\RetailServer\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="0e99e-713">Packages\RetailServer\Sdk.RetailServerSetup.proj</span></span>
  
  - <span data-ttu-id="0e99e-714">**Sdk.ModernPos.Shared.csproj** ファイルの場合</span><span class="sxs-lookup"><span data-stu-id="0e99e-714">For the **Sdk.ModernPos.Shared.csproj** file</span></span> 
    - <span data-ttu-id="0e99e-715">**ItemGroup** セクションに新しい行を追加</span><span class="sxs-lookup"><span data-stu-id="0e99e-715">Add line to the **ItemGroup** section</span></span>
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > <span data-ttu-id="0e99e-716"><ファイル名> ではなく、リソース ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-716">Instead of the <File_name> specify a name of the resource file.</span></span> <span data-ttu-id="0e99e-717">次に示す例にも同じことが当てはまります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-717">The same is relevant for the other examples given below.</span></span>
 
    - <span data-ttu-id="0e99e-718">**Target Name="CopyPackageFiles"** セクションに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-718">Add line to the **Target Name="CopyPackageFiles"** section</span></span>
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - <span data-ttu-id="0e99e-719">**Sdk.RetailServerSetup.proj** ファイルの場合</span><span class="sxs-lookup"><span data-stu-id="0e99e-719">For the **Sdk.RetailServerSetup.proj** file</span></span> 
    - <span data-ttu-id="0e99e-720">**ItemGroup** セクションに新しい行を追加</span><span class="sxs-lookup"><span data-stu-id="0e99e-720">Add line to the **ItemGroup** section</span></span>
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - <span data-ttu-id="0e99e-721">**Target Name="CopyPackageFiles"** セクションに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-721">Add line to the **Target Name="CopyPackageFiles"** section</span></span>
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. <span data-ttu-id="0e99e-722">拇印、保管場所、署名販売取引に使用されるべき証明書の保存名を指定して、証明書のコンフィギュレーションを変更します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-722">Modify the certificate's configuration file by specifying the thumbprint, store location, and store name for the certificate that should be used to sign sales transactions.</span></span> <span data-ttu-id="0e99e-723">その後 **References** フォルダーにコンフィギュレーション ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-723">Then copy the configuration file to the **References** folder.</span></span>

    # <a name="application-update-4"></a>[<span data-ttu-id="0e99e-724">アプリケーション 更新 4</span><span class="sxs-lookup"><span data-stu-id="0e99e-724">Application update 4</span></span>](#tab/app-update-4)

    <span data-ttu-id="0e99e-725">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-725">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="application-update-5-and-later"></a>[<span data-ttu-id="0e99e-726">アプリケーション更新プログラム 5 以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-726">Application update 5 and later</span></span>](#tab/app-update-5-and-later)

    <span data-ttu-id="0e99e-727">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-727">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="0e99e-728">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="0e99e-728">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    <span data-ttu-id="0e99e-729">ファイル名は **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** で、**CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-729">The file is named **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, and it's under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="0e99e-730">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-730">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    <span data-ttu-id="0e99e-731">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-731">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-735-and-later"></a>[<span data-ttu-id="0e99e-732">Retail 7.3.5 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-732">Retail 7.3.5 and later</span></span>](#tab/retail-7-3-5)

    <span data-ttu-id="0e99e-733">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-733">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    # <a name="retail-811-and-later"></a>[<span data-ttu-id="0e99e-734">Retail 8.1.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="0e99e-734">Retail 8.1.1 and later</span></span>](#tab/retail-8-1-1)

    <span data-ttu-id="0e99e-735">ファイル名は **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** で、**Extensions.SequentialSignatureRegister\\bin\\Debug** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-735">The file is named **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, and it's under **Extensions.SequentialSignatureRegister\\bin\\Debug**.</span></span>

    ---

6. <span data-ttu-id="0e99e-736">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-736">Update Retail Server configuration file.</span></span> <span data-ttu-id="0e99e-737">**RetailSDK\\Packages\\RetailServer\\Code\\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-737">In the **RetailSDK\\Packages\\RetailServer\\Code\\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. <span data-ttu-id="0e99e-738">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-738">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
8. <span data-ttu-id="0e99e-739">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-739">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="0e99e-740">詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e99e-740">For more information, see [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a><span data-ttu-id="0e99e-741">Modern POS のオフライン モードでのデジタル署名を有効にします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-741">Enable the digital signature in offline mode for Modern POS</span></span>

<span data-ttu-id="0e99e-742">Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e99e-742">To enable the digital signature in offline mode for Modern POS, you must follow these steps after you activate Modern POS on a new device.</span></span>

1. <span data-ttu-id="0e99e-743">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-743">Sign in to POS.</span></span>
2. <span data-ttu-id="0e99e-744">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-744">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="0e99e-745">**ダウンロードの保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="0e99e-745">When the value of the **Pending downloads** field is **0** (zero), the database is fully synchronized.</span></span>
3. <span data-ttu-id="0e99e-746">POS からのサインアウト</span><span class="sxs-lookup"><span data-stu-id="0e99e-746">Sign out of POS.</span></span>
4. <span data-ttu-id="0e99e-747">オフライン データベースが完全に同期するため少しの間待ちます。</span><span class="sxs-lookup"><span data-stu-id="0e99e-747">Wait a while for the offline database to be fully synchronized.</span></span>
5. <span data-ttu-id="0e99e-748">POS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="0e99e-748">Sign in to POS.</span></span>
6. <span data-ttu-id="0e99e-749">**データベースの接続の状態** ページで、オフライン データベースが完全に同期化されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-749">On the **Database connection status** page, make sure that the offline database is fully synchronized.</span></span> <span data-ttu-id="0e99e-750">**オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の時、データベースは完全に同期しています。</span><span class="sxs-lookup"><span data-stu-id="0e99e-750">When the value of the **Pending transactions in offline database** field is **0** (zero), the database is fully synchronized.</span></span>
7. <span data-ttu-id="0e99e-751">Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="0e99e-751">Restart Modern POS.</span></span>
