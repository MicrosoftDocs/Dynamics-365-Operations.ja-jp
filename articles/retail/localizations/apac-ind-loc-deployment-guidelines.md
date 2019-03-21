---
title: インドのキャッシュ レジスターの配置ガイドライン
description: このトピックは、インドの小売ローカライズ用配置ガイドです。
author: AlexChern0v
manager: ralin
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: shylaw
ms.search.region: India
ms.search.industry: Retail
ms.author: jiaqia
ms.search.scope: Retail
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: a636ddaf42c4545cfd3c988d34f00e35cf714545
ms.sourcegitcommit: 2cf5498098e7a5ade1c16eac6df26bc98e4565cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2019
ms.locfileid: "760767"
---
# <a name="deployment-guidelines-for-cash-registers-for-india"></a><span data-ttu-id="e4017-103">インドのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="e4017-103">Deployment guidelines for cash registers for India</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4017-104">このトピックは、インドの Microsoft Dynamics 365 for Retail ローカライズで商品及びサービス税 (GST) の要件を有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="e4017-104">This topic is a deployment guide that shows how to enable the requirements for Goods and Services Tax (GST) in the Microsoft Dynamics 365 for Retail localization for India.</span></span> <span data-ttu-id="e4017-105">インドの小売ローカライズの詳細については、[インドのキャッシュ レジスターの販売税統合](./apac-ind-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4017-105">For more information about the Retail localization for India, see [GST integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

<span data-ttu-id="e4017-106">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="e4017-106">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="e4017-107">リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4017-107">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="e4017-108">このサンプルは Commerce runtime (CRT) の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="e4017-108">This sample consists of extensions for the Commerce runtime (CRT).</span></span> <span data-ttu-id="e4017-109">このサンプルを実行するには、CRT プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4017-109">To run this sample, you must modify and build the CRT projects.</span></span> <span data-ttu-id="e4017-110">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e4017-110">We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="e4017-111">また Microsoft Visual Studio オンライン (VSO) のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e4017-111">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="e4017-112">使用しているバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="e4017-112">Some steps in the procedures in this topic differ, depending on the version of Retail that you're using.</span></span> <span data-ttu-id="e4017-113">詳細については、[Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4017-113">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4017-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="e4017-114">Prerequisites</span></span>

<span data-ttu-id="e4017-115">Visual C++ 再頒布可能パッケージが商品及びサービス税 (GST) 計算を実行するマシン上にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e4017-115">Make sure that the Visual C++ Redistributable Packages are present on the machine that you're running Goods and Services Tax (GST) calculations on.</span></span> <span data-ttu-id="e4017-116">クラウド POS、およびオンライン モードの Modern POS の場合、このマシンは小売サーバーです。</span><span class="sxs-lookup"><span data-stu-id="e4017-116">For Cloud POS, and for Modern POS in online mode, this machine is Retail server.</span></span> <span data-ttu-id="e4017-117">オフライン モードの Modern POS の場合、それは Modern POS マシン自身です。</span><span class="sxs-lookup"><span data-stu-id="e4017-117">For Modern POS in offline mode, it's the Modern POS machine itself.</span></span> <span data-ttu-id="e4017-118">パッケージを取得するには、[Visual C++ 再頒布可能パッケージをダウンロード](https://www.microsoft.com/download/details.aspx?id=30679)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4017-118">To get the packages, see [Download the Visual C++ Redistributable Packages](https://www.microsoft.com/download/details.aspx?id=30679).</span></span>

## <a name="development-environment"></a><span data-ttu-id="e4017-119">開発環境</span><span class="sxs-lookup"><span data-stu-id="e4017-119">Development environment</span></span>

<span data-ttu-id="e4017-120">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e4017-120">Follow these steps to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="e4017-121">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="e4017-121">The CRT extension components</span></span>

<span data-ttu-id="e4017-122">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e4017-122">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="e4017-123">次の手順を完了するには、CRT ソリューション **CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="e4017-123">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**.</span></span> <span data-ttu-id="e4017-124">このソリューションは **RetailSdk\\SampleExtensions\\CommerceRuntime** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-124">You can find this solution under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

#### <a name="generic-tax-engine-component"></a><span data-ttu-id="e4017-125">汎用税エンジン コンポーネント</span><span class="sxs-lookup"><span data-stu-id="e4017-125">Generic Tax Engine component</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="e4017-126">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="e4017-126">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

1. <span data-ttu-id="e4017-127">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="e4017-127">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="e4017-128">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="e4017-128">Find the following files:</span></span>

    - <span data-ttu-id="e4017-129">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-129">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="e4017-130">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-130">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="e4017-131">**Reference\\Newtonsoft.Json\\9.0.0.0** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-131">In the **Reference\\Newtonsoft.Json\\9.0.0.0** folder:</span></span>

        - <span data-ttu-id="e4017-132">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-132">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="e4017-133">**Reference\\TaxEngine** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-133">In the **Reference\\TaxEngine** folder:</span></span>

        - <span data-ttu-id="e4017-134">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-134">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="e4017-135">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-135">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="e4017-136">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-136">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="e4017-137">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-137">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="e4017-138">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-138">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>
        - <span data-ttu-id="e4017-139">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-139">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="e4017-140">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-140">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="e4017-141">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-141">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="e4017-142">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-142">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="e4017-143">以下のフォルダーを **Reference\\Z3** フォルダー内で見つけます:</span><span class="sxs-lookup"><span data-stu-id="e4017-143">Find the following folders in the **Reference\\Z3** folder:</span></span>

        - <span data-ttu-id="e4017-144">x86</span><span class="sxs-lookup"><span data-stu-id="e4017-144">x86</span></span>
        - <span data-ttu-id="e4017-145">x64</span><span class="sxs-lookup"><span data-stu-id="e4017-145">x64</span></span>

3. <span data-ttu-id="e4017-146">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="e4017-146">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="e4017-147">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e4017-147">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="e4017-148">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e4017-148">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="e4017-149">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="e4017-149">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="e4017-150">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-150">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="e4017-151">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-151">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="e4017-152">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="e4017-152">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="e4017-153">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="e4017-153">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="e4017-154">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="e4017-154">These files aren't intended for any customizations.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="e4017-155">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-155">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

1. <span data-ttu-id="e4017-156">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="e4017-156">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="e4017-157">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="e4017-157">Find the following files:</span></span>

    - <span data-ttu-id="e4017-158">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-158">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="e4017-159">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-159">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="e4017-160">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-160">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="e4017-161">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-161">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="e4017-162">**References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-162">In the **References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="e4017-163">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-163">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="e4017-164">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-164">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="e4017-165">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-165">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="e4017-166">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-166">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="e4017-167">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-167">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="e4017-168">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-168">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="e4017-169">**References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-169">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="e4017-170">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-170">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="e4017-171">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-171">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="e4017-172">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-172">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="e4017-173">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="e4017-173">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="e4017-174">x86</span><span class="sxs-lookup"><span data-stu-id="e4017-174">x86</span></span>
        - <span data-ttu-id="e4017-175">x64</span><span class="sxs-lookup"><span data-stu-id="e4017-175">x64</span></span>

3. <span data-ttu-id="e4017-176">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="e4017-176">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="e4017-177">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e4017-177">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="e4017-178">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e4017-178">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="e4017-179">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="e4017-179">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="e4017-180">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-180">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="e4017-181">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-181">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="e4017-182">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="e4017-182">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="e4017-183">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="e4017-183">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="e4017-184">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="e4017-184">These files aren't intended for any customizations.</span></span>

# <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="e4017-185">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-185">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

1. <span data-ttu-id="e4017-186">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="e4017-186">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="e4017-187">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="e4017-187">Find the following files:</span></span>

    - <span data-ttu-id="e4017-188">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-188">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="e4017-189">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-189">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="e4017-190">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-190">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="e4017-191">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-191">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="e4017-192">**References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-192">In the **References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="e4017-193">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-193">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="e4017-194">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-194">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="e4017-195">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-195">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="e4017-196">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-196">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="e4017-197">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-197">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="e4017-198">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-198">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="e4017-199">**References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="e4017-199">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="e4017-200">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-200">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="e4017-201">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-201">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="e4017-202">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="e4017-202">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="e4017-203">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="e4017-203">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="e4017-204">x86</span><span class="sxs-lookup"><span data-stu-id="e4017-204">x86</span></span>
        - <span data-ttu-id="e4017-205">x64</span><span class="sxs-lookup"><span data-stu-id="e4017-205">x64</span></span>

3. <span data-ttu-id="e4017-206">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="e4017-206">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="e4017-207">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e4017-207">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="e4017-208">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="e4017-208">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="e4017-209">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="e4017-209">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="e4017-210">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-210">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="e4017-211">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-211">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="e4017-212">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="e4017-212">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="e4017-213">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="e4017-213">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="e4017-214">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="e4017-214">These files aren't intended for any customizations.</span></span>

# <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="e4017-215">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-215">Retail 10.0 and later</span></span>](#tab/retail-10-0)

<span data-ttu-id="e4017-216">汎用税エンジン コンポーネントはシールド拡張機能の一部です。</span><span class="sxs-lookup"><span data-stu-id="e4017-216">The Generic Tax Engine component is a part of sealed extensions.</span></span>

1. <span data-ttu-id="e4017-217">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="e4017-217">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="e4017-218">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-218">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="e4017-219">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="e4017-219">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="e4017-220">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="e4017-220">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="e4017-221">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="e4017-221">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="e4017-222">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="e4017-222">These files aren't intended for any customizations.</span></span>

---

### <a name="set-up-required-parameters-in-retail-headquarters"></a><span data-ttu-id="e4017-223">小売用バックオフィスで要求されるパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="e4017-223">Set up required parameters in Retail headquarters</span></span>

<span data-ttu-id="e4017-224">詳細については、[インドのキャッシュ レジスターの販売税統合](./apac-ind-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4017-224">For more information, see [GST integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="e4017-225">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="e4017-225">Production environment</span></span>

<span data-ttu-id="e4017-226">以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、パッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="e4017-226">Follow these steps to create deployable packages that contain Retail components, and to apply the packages in a production environment.</span></span>

1. <span data-ttu-id="e4017-227">**RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-227">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files under the **RetailSdk\\Assets** folder, add the following lines to the **composition** section.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="e4017-228">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="e4017-228">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="e4017-229">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-229">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="e4017-230">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-230">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="e4017-231">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-231">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    ---

2. <span data-ttu-id="e4017-232">**RetailSdk\\BuildTools** フォルダーの下の **Customization.settings** パッケージ カスタマイズ構成ファイルで、以下の行を **ItemGroup** セクションに追加して、配置可能パッケージ内の CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="e4017-232">In the **Customization.settings** package customization configuration file under the **RetailSdk\\BuildTools** folder, add the following lines to the **ItemGroup** section to include the CRT extensions in deployable packages.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="e4017-233">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="e4017-233">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.Core.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.Metadata.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.DataAccessor.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.DataAccessFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.DataModel.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.LocalizationFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.LocalizationFrameworkCore.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.ElectronicReportingMapping.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.XppSupportLayer.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Newtonsoft.Json\9.0.0.0\Newtonsoft.Json.dll" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="e4017-234">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-234">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.GenericTaxEngine.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Core.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Metadata.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessor.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataModel.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.LocalizationFrameworkCore.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.ElectronicReportingMapping.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.XppSupportLayer.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Newtonsoft.Json.9.0.1\lib\net45\Newtonsoft.Json.dll" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="e4017-235">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-235">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.GenericTaxEngine.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Core.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Metadata.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessor.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataModel.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.LocalizationFrameworkCore.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.ElectronicReportingMapping.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.XppSupportLayer.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Newtonsoft.Json.9.0.1\lib\net45\Newtonsoft.Json.dll" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="e4017-236">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-236">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="e4017-237">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="e4017-237">This step doesn't apply to this version.</span></span>

    ---

3. <span data-ttu-id="e4017-238">以下のファイルを修正して、配置可能パッケージに Z3 ライブラリを含めます。</span><span class="sxs-lookup"><span data-stu-id="e4017-238">Modify the following files to include the Z3 libraries in deployable packages:</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="e4017-239">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="e4017-239">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="e4017-240">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="e4017-240">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="e4017-241">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="e4017-241">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="e4017-242">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="e4017-242">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="e4017-243">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-243">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="..\..\References\Z3\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="..\..\References\Z3\x64\*.*" />
    ```

    <span data-ttu-id="e4017-244">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-244">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="e4017-245">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-245">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>
    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="e4017-246">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-246">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="e4017-247">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="e4017-247">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="e4017-248">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="e4017-248">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="e4017-249">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="e4017-249">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="e4017-250">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-250">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
    ```

    <span data-ttu-id="e4017-251">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-251">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="e4017-252">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-252">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="e4017-253">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-253">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    - <span data-ttu-id="e4017-254">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span><span class="sxs-lookup"><span data-stu-id="e4017-254">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span></span>
    - <span data-ttu-id="e4017-255">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="e4017-255">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="e4017-256">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-256">Add the following lines to the **ItemGroup** section.</span></span>

     ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
     ```

    <span data-ttu-id="e4017-257">**Sdk.ModernPos.Shared.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-257">For **Sdk.ModernPos.Shared.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="e4017-258">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e4017-258">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="e4017-259">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="e4017-259">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="e4017-260">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="e4017-260">This step doesn't apply to this version.</span></span>

    ---

4. <span data-ttu-id="e4017-261">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="e4017-261">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
5. <span data-ttu-id="e4017-262">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="e4017-262">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="e4017-263">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4017-263">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>
