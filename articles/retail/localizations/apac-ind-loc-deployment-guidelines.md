---
title: インドのキャッシュ レジスターの配置ガイドライン
description: このトピックは、インドの小売ローカライズ用配置ガイドです。
author: AlexChern0v
manager: annbe
ms.date: 09/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: India
ms.search.industry: Retail
ms.author: jiaqia
ms.search.scope: Retail
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: 969e9ffaa541b3a1d5f8c3aeb41838021cb7521c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025480"
---
# <a name="deployment-guidelines-for-cash-registers-for-india"></a><span data-ttu-id="bce71-103">インドのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="bce71-103">Deployment guidelines for cash registers for India</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bce71-104">このトピックは、インドの Dynamics 365 Retail ローカライズで商品及びサービス税 (GST) の要件を有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="bce71-104">This topic is a deployment guide that shows how to enable the requirements for Goods and Services Tax (GST) in the Dynamics 365 Retail localization for India.</span></span> <span data-ttu-id="bce71-105">インドの小売ローカライズの詳細については、[インドのキャッシュ レジスターの販売税統合](./apac-ind-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bce71-105">For more information about the Retail localization for India, see [GST integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

<span data-ttu-id="bce71-106">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="bce71-106">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="bce71-107">リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bce71-107">For information about how to install and use the Retail SDK, see the [Retail SDK documentation](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="bce71-108">このサンプルは Commerce runtime (CRT) の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="bce71-108">This sample consists of extensions for the Commerce runtime (CRT).</span></span> <span data-ttu-id="bce71-109">このサンプルを実行するには、CRT プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bce71-109">To run this sample, you must modify and build the CRT projects.</span></span> <span data-ttu-id="bce71-110">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bce71-110">We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="bce71-111">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="bce71-111">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="bce71-112">使用しているバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="bce71-112">Some steps in the procedures in this topic differ, depending on the version of Retail that you're using.</span></span> <span data-ttu-id="bce71-113">詳細については、[Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bce71-113">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bce71-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="bce71-114">Prerequisites</span></span>

<span data-ttu-id="bce71-115">Visual C++ 再頒布可能パッケージが商品及びサービス税 (GST) 計算を実行するマシン上にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bce71-115">Make sure that the Visual C++ Redistributable Packages are present on the machine that you're running Goods and Services Tax (GST) calculations on.</span></span> <span data-ttu-id="bce71-116">クラウド POS、およびオンライン モードの Modern POS の場合、このマシンは小売サーバーです。</span><span class="sxs-lookup"><span data-stu-id="bce71-116">For Cloud POS, and for Modern POS in online mode, this machine is Retail server.</span></span> <span data-ttu-id="bce71-117">オフライン モードの Modern POS の場合、それは Modern POS マシン自身です。</span><span class="sxs-lookup"><span data-stu-id="bce71-117">For Modern POS in offline mode, it's the Modern POS machine itself.</span></span> <span data-ttu-id="bce71-118">パッケージを取得するには、[Visual C++ 再頒布可能パッケージをダウンロード](https://www.microsoft.com/download/details.aspx?id=48145)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bce71-118">To get the packages, see [Download the Visual C++ Redistributable Packages](https://www.microsoft.com/download/details.aspx?id=48145).</span></span>

## <a name="development-environment"></a><span data-ttu-id="bce71-119">開発環境</span><span class="sxs-lookup"><span data-stu-id="bce71-119">Development environment</span></span>

<span data-ttu-id="bce71-120">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bce71-120">Follow these steps to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="bce71-121">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bce71-121">The CRT extension components</span></span>

<span data-ttu-id="bce71-122">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bce71-122">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="bce71-123">次の手順を完了するには、CRT ソリューション **CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="bce71-123">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**.</span></span> <span data-ttu-id="bce71-124">このソリューションは **RetailSdk\\SampleExtensions\\CommerceRuntime** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-124">You can find this solution under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-125">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-125">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

1. <span data-ttu-id="bce71-126">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="bce71-126">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="bce71-127">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="bce71-127">Find the following files:</span></span>

    - <span data-ttu-id="bce71-128">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-128">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="bce71-129">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-129">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="bce71-130">**Reference\\Newtonsoft.Json\\9.0.0.0** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-130">In the **Reference\\Newtonsoft.Json\\9.0.0.0** folder:</span></span>

        - <span data-ttu-id="bce71-131">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-131">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="bce71-132">**Reference\\TaxEngine** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-132">In the **Reference\\TaxEngine** folder:</span></span>

        - <span data-ttu-id="bce71-133">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-133">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="bce71-134">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-134">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="bce71-135">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-135">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="bce71-136">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-136">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="bce71-137">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-137">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>
        - <span data-ttu-id="bce71-138">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-138">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="bce71-139">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-139">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="bce71-140">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-140">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="bce71-141">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-141">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="bce71-142">以下のフォルダーを **Reference\\Z3** フォルダー内で見つけます:</span><span class="sxs-lookup"><span data-stu-id="bce71-142">Find the following folders in the **Reference\\Z3** folder:</span></span>

        - <span data-ttu-id="bce71-143">x86</span><span class="sxs-lookup"><span data-stu-id="bce71-143">x86</span></span>
        - <span data-ttu-id="bce71-144">x64</span><span class="sxs-lookup"><span data-stu-id="bce71-144">x64</span></span>

3. <span data-ttu-id="bce71-145">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="bce71-145">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="bce71-146">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="bce71-146">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="bce71-147">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="bce71-147">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="bce71-148">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="bce71-148">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="bce71-149">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-149">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="bce71-150">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-150">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="bce71-151">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="bce71-151">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="bce71-152">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="bce71-152">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="bce71-153">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="bce71-153">These files aren't intended for any customizations.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-154">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-154">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

1. <span data-ttu-id="bce71-155">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="bce71-155">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="bce71-156">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="bce71-156">Find the following files:</span></span>

    - <span data-ttu-id="bce71-157">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-157">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="bce71-158">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-158">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="bce71-159">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-159">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="bce71-160">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-160">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="bce71-161">**References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-161">In the **References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="bce71-162">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-162">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="bce71-163">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-163">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="bce71-164">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-164">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="bce71-165">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-165">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="bce71-166">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-166">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="bce71-167">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-167">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="bce71-168">**References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-168">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="bce71-169">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-169">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="bce71-170">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-170">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="bce71-171">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-171">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="bce71-172">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="bce71-172">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="bce71-173">x86</span><span class="sxs-lookup"><span data-stu-id="bce71-173">x86</span></span>
        - <span data-ttu-id="bce71-174">x64</span><span class="sxs-lookup"><span data-stu-id="bce71-174">x64</span></span>

3. <span data-ttu-id="bce71-175">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="bce71-175">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="bce71-176">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="bce71-176">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="bce71-177">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="bce71-177">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="bce71-178">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="bce71-178">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="bce71-179">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-179">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="bce71-180">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-180">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="bce71-181">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="bce71-181">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="bce71-182">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="bce71-182">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="bce71-183">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="bce71-183">These files aren't intended for any customizations.</span></span>

# <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-184">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-184">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

1. <span data-ttu-id="bce71-185">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="bce71-185">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="bce71-186">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="bce71-186">Find the following files:</span></span>

    - <span data-ttu-id="bce71-187">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-187">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="bce71-188">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-188">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="bce71-189">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-189">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="bce71-190">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-190">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="bce71-191">**References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-191">In the **References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="bce71-192">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-192">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="bce71-193">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-193">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="bce71-194">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-194">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="bce71-195">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-195">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="bce71-196">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-196">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="bce71-197">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-197">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="bce71-198">**References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="bce71-198">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="bce71-199">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-199">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="bce71-200">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-200">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="bce71-201">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="bce71-201">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="bce71-202">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="bce71-202">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="bce71-203">x86</span><span class="sxs-lookup"><span data-stu-id="bce71-203">x86</span></span>
        - <span data-ttu-id="bce71-204">x64</span><span class="sxs-lookup"><span data-stu-id="bce71-204">x64</span></span>

3. <span data-ttu-id="bce71-205">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="bce71-205">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="bce71-206">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="bce71-206">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="bce71-207">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="bce71-207">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="bce71-208">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="bce71-208">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="bce71-209">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-209">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="bce71-210">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-210">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="bce71-211">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="bce71-211">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="bce71-212">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="bce71-212">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="bce71-213">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="bce71-213">These files aren't intended for any customizations.</span></span>

# <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-214">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-214">Retail 10.0 and later</span></span>](#tab/retail-10-0)

<span data-ttu-id="bce71-215">汎用税エンジン コンポーネントはシールド拡張機能の一部です。</span><span class="sxs-lookup"><span data-stu-id="bce71-215">The Generic Tax Engine component is a part of sealed extensions.</span></span>

1. <span data-ttu-id="bce71-216">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="bce71-216">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="bce71-217">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-217">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="bce71-218">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-218">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="bce71-219">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="bce71-219">Register the CRT change in the extensions configuration file:</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="bce71-220">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては*いけません*。</span><span class="sxs-lookup"><span data-stu-id="bce71-220">Do *not* edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="bce71-221">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="bce71-221">These files aren't intended for any customizations.</span></span>

# <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-222">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-222">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="bce71-223">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="bce71-223">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="bce71-224">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-224">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="bce71-225">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="bce71-225">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="bce71-226">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="bce71-226">Register the CRT change in the extensions configuration file:</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="bce71-227">上に示すように、拡張機能の順序を保持します。</span><span class="sxs-lookup"><span data-stu-id="bce71-227">Keep the order of the extensions as shown above.</span></span>

    > [!WARNING]
    > <span data-ttu-id="bce71-228">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="bce71-228">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="bce71-229">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="bce71-229">These files aren't intended for any customizations.</span></span>

---

### <a name="the-retail-server-extension-components"></a><span data-ttu-id="bce71-230">Retail Server 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bce71-230">The Retail Server extension components</span></span>

1. <span data-ttu-id="bce71-231">IIS Retail Server サイトがある場所の下にあるルート フォルダーの **web.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="bce71-231">Open **web.config** in the root folder under the IIS Retail Server site location.</span></span>
2. <span data-ttu-id="bce71-232">コンフィギュレーションの **extensionComposition** セクションで Retail Server 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="bce71-232">Register the Retail Server extensions in the **extensionComposition** section of the configuration file.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-233">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-233">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="bce71-234">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-234">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-235">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-235">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="bce71-236">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-236">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-237">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-237">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="bce71-238">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-238">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-239">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-239">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="bce71-240">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-240">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-241">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-241">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

``` xml
<add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
```

---
### <a name="the-clientbroker-extension-components"></a><span data-ttu-id="bce71-242">ClientBroker 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bce71-242">The ClientBroker extension components</span></span>

1. <span data-ttu-id="bce71-243">ローカル CRT クライアント ブローカーの場所の下にある **RetailProxy.MPOSOffline.ext.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="bce71-243">Open **RetailProxy.MPOSOffline.ext.config** under the local CRT client broker location.</span></span>
2. <span data-ttu-id="bce71-244">コンフィギュレーション ファイルの **extensionComposition** セクションで Retail Proxy 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="bce71-244">Register the Retail Proxy extensions in the **extensionComposition** section of the configuration file.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-245">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-245">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="bce71-246">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-246">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-247">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-247">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="bce71-248">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-248">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-249">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-249">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="bce71-250">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-250">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-251">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-251">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="bce71-252">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-252">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-253">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-253">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

``` xml
<add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
```

---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="bce71-254">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bce71-254">The Modern POS extension components</span></span>

<span data-ttu-id="bce71-255">税登録の ID 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bce71-255">Enable the Tax Registration Id extension.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-256">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-256">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="bce71-257">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-257">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-258">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-258">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="bce71-259">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-259">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-260">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-260">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="bce71-261">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-261">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-262">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-262">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="bce71-263">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-263">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-264">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-264">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="bce71-265">**RetailSdk\POS\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="bce71-265">Open the solution at **RetailSdk\POS\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="bce71-266">また、Modern POS が Run コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bce71-266">Also make sure that Modern POS can be run from Microsoft Visual Studio using the Run command.</span></span> <span data-ttu-id="bce71-267">(Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="bce71-267">(Modern POS must not be customized.</span></span> <span data-ttu-id="bce71-268">ユーザー アカウント制御 [UAC] を有効にして、以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。)</span><span class="sxs-lookup"><span data-stu-id="bce71-268">You must enable User Account Control [UAC], and uninstall previously installed instances of Modern POS.)</span></span>

2. <span data-ttu-id="bce71-269">**POS.Extensions\extensions.json** で、次の行を追加することによって拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bce71-269">Enable the extension in **POS.Extensions\extensions.json** by adding the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. <span data-ttu-id="bce71-270">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="bce71-270">Build the solution.</span></span>
4. <span data-ttu-id="bce71-271">Modern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="bce71-271">Run Modern POS and test the functionality.</span></span>

---

### <a name="the-cloud-pos-extension-components"></a><span data-ttu-id="bce71-272">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bce71-272">The Cloud POS extension components</span></span>

<span data-ttu-id="bce71-273">税登録の ID 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bce71-273">Enable the Tax Registration Id extension.</span></span>

# <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-274">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-274">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="bce71-275">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-275">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-276">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-276">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="bce71-277">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-277">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-278">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-278">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="bce71-279">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-279">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-280">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-280">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="bce71-281">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-281">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-282">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-282">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="bce71-283">**RetailSdk\POS\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="bce71-283">Open the solution at **RetailSdk\POS\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="bce71-284">**POS.Extensions\extensions.json** で、次の行を追加することによって拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bce71-284">Enable the extension in **POS.Extensions\extensions.json** by adding the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. <span data-ttu-id="bce71-285">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="bce71-285">Build the solution.</span></span>
4. <span data-ttu-id="bce71-286">クラウド POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="bce71-286">Run Cloud POS and test the functionality.</span></span>

---

### <a name="set-up-required-parameters-in-retail-headquarters"></a><span data-ttu-id="bce71-287">小売用バックオフィスで要求されるパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="bce71-287">Set up required parameters in Retail headquarters</span></span>

<span data-ttu-id="bce71-288">詳細については、[インドのキャッシュ レジスターの販売税統合](./apac-ind-cash-registers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bce71-288">For more information, see [GST integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="bce71-289">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="bce71-289">Production environment</span></span>

<span data-ttu-id="bce71-290">以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、パッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="bce71-290">Follow these steps to create deployable packages that contain Retail components, and to apply the packages in a production environment.</span></span>

1. <span data-ttu-id="bce71-291">**RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-291">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files under the **RetailSdk\\Assets** folder, add the following lines to the **composition** section.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-292">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-292">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-293">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-293">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-294">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-294">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-295">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-295">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-296">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-296">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="bce71-297">上に示すように、拡張機能の順序を保持します。</span><span class="sxs-lookup"><span data-stu-id="bce71-297">Keep the order of the extensions as shown above.</span></span>

    ---

2. <span data-ttu-id="bce71-298">**RetailSdk\\Assets** フォルダーの下の **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、以下の行を**合成**セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-298">In the **RetailProxy.MPOSOffline.ext.config** configuration file under the **RetailSdk\\Assets** folder, add the following lines to the **composition** section.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-299">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-299">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="bce71-300">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-300">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-301">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-301">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="bce71-302">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-302">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-303">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-303">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="bce71-304">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-304">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-305">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-305">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="bce71-306">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-306">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-307">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-307">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
    ```

    ---

3. <span data-ttu-id="bce71-308">Retail Server コンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="bce71-308">Update the Retail Server configuration file.</span></span> <span data-ttu-id="bce71-309">**RetailSDK\Packages\RetailServer\Code\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-309">In the **RetailSDK\Packages\RetailServer\Code\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-310">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-310">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="bce71-311">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-311">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-312">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-312">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="bce71-313">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-313">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-314">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-314">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="bce71-315">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-315">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-316">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-316">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="bce71-317">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-317">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-318">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-318">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
    ```

    ---

4. <span data-ttu-id="bce71-319">**RetailSdk\\BuildTools** フォルダーの下の **Customization.settings** パッケージ カスタマイズ構成ファイルで、以下の行を **ItemGroup** セクションに追加して、配置可能パッケージ内の CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="bce71-319">In the **Customization.settings** package customization configuration file under the **RetailSdk\\BuildTools** folder, add the following lines to the **ItemGroup** section to include the CRT extensions in deployable packages.</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-320">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-320">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

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

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-321">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-321">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-322">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-322">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

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

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-323">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-323">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="bce71-324">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-324">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-325">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-325">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    > [!NOTE]
    > <span data-ttu-id="bce71-326">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-326">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="bce71-327">以下のファイルを修正して、配置可能パッケージに Z3 ライブラリを含めます。</span><span class="sxs-lookup"><span data-stu-id="bce71-327">Modify the following files to include the Z3 libraries in deployable packages:</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-328">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-328">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="bce71-329">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="bce71-329">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="bce71-330">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="bce71-330">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="bce71-331">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="bce71-331">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="bce71-332">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-332">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="..\..\References\Z3\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="..\..\References\Z3\x64\*.*" />
    ```

    <span data-ttu-id="bce71-333">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-333">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="bce71-334">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-334">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>
    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-335">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-335">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="bce71-336">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="bce71-336">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="bce71-337">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="bce71-337">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="bce71-338">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="bce71-338">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="bce71-339">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-339">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
    ```

    <span data-ttu-id="bce71-340">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-340">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="bce71-341">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-341">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-342">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-342">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    - <span data-ttu-id="bce71-343">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span><span class="sxs-lookup"><span data-stu-id="bce71-343">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span></span>
    - <span data-ttu-id="bce71-344">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="bce71-344">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="bce71-345">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-345">Add the following lines to the **ItemGroup** section.</span></span>

     ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
     ```

    <span data-ttu-id="bce71-346">**Sdk.ModernPos.Shared.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-346">For **Sdk.ModernPos.Shared.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="bce71-347">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-347">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-348">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-348">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="bce71-349">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-349">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-350">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-350">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    > [!NOTE]
    > <span data-ttu-id="bce71-351">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-351">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="bce71-352">税登録の ID POS 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bce71-352">Enable the Tax Registration Id POS extension:</span></span>

    # <a name="retail-731tabretail-7-3-1"></a>[<span data-ttu-id="bce71-353">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="bce71-353">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="bce71-354">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-354">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[<span data-ttu-id="bce71-355">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-355">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="bce71-356">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-356">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[<span data-ttu-id="bce71-357">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-357">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="bce71-358">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-358">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-latertabretail-10-0"></a>[<span data-ttu-id="bce71-359">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-359">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="bce71-360">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="bce71-360">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-latertabretail-10-0-6"></a>[<span data-ttu-id="bce71-361">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="bce71-361">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    <span data-ttu-id="bce71-362">**RetailSDK\POS\Extensions\extensions.json** を開いて、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="bce71-362">Open **RetailSDK\POS\Extensions\extensions.json** and add the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

7. <span data-ttu-id="bce71-363">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="bce71-363">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
8. <span data-ttu-id="bce71-364">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="bce71-364">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="bce71-365">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bce71-365">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>
