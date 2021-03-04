---
title: インドのキャッシュ レジスターの配置ガイドライン
description: このトピックは、インドのローカライズ用配置ガイドです。
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
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: fea0710e502cd57ebb9cd3f1817acaf2d00fb7a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972771"
---
# <a name="deployment-guidelines-for-cash-registers-for-india"></a><span data-ttu-id="35b14-103">インドのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="35b14-103">Deployment guidelines for cash registers for India</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35b14-104">このトピックは、インドの Dynamics 365 Commerce アプリのローカライズで商品及びサービス税 (GST) の要件を有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="35b14-104">This topic is a deployment guide that shows how to enable the requirements for Goods and Services Tax (GST) in the Dynamics 365 Commerce app's localization for India.</span></span> <span data-ttu-id="35b14-105">インドのローカライズの詳細については、[インド向けのキャッシュ レジスターの商品及びサービス税 (GST) 統合](./apac-ind-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35b14-105">For more information about the localization for India, see [Goods and Services Tax (GST) integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

<span data-ttu-id="35b14-106">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="35b14-106">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="35b14-107">SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35b14-107">For information about how to install and use the SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="35b14-108">このサンプルは Commerce runtime (CRT) の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="35b14-108">This sample consists of extensions for the Commerce runtime (CRT).</span></span> <span data-ttu-id="35b14-109">このサンプルを実行するには、CRT プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35b14-109">To run this sample, you must modify and build the CRT projects.</span></span> <span data-ttu-id="35b14-110">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="35b14-110">We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="35b14-111">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="35b14-111">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="35b14-112">使用しているアプリのバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="35b14-112">Some steps in the procedures in this topic differ, depending on the version of the app that you're using.</span></span> <span data-ttu-id="35b14-113">詳細については、 [Dynamics 365 Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35b14-113">For more information, see [What's new or changed in Dynamics 365 Retail](../get-started/whats-new.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="35b14-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="35b14-114">Prerequisites</span></span>

<span data-ttu-id="35b14-115">Visual C++ 再頒布可能パッケージが商品及びサービス税 (GST) 計算を実行するマシン上にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="35b14-115">Make sure that the Visual C++ Redistributable Packages are present on the machine that you're running Goods and Services Tax (GST) calculations on.</span></span> <span data-ttu-id="35b14-116">クラウド POS、およびオンライン モードの Modern POS の場合は、このマシンは小売サーバーとなります (小売サーバーは、コマース 10.0.8 とそれ以降で Commerce Scale Unit と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="35b14-116">For Cloud POS, and for Modern POS in online mode, this machine is Retail Server (Retail Server is known as Commerce Scale Unit in Commerce 10.0.8 and above).</span></span> <span data-ttu-id="35b14-117">オフライン モードの Modern POS の場合、それは Modern POS マシン自身です。</span><span class="sxs-lookup"><span data-stu-id="35b14-117">For Modern POS in offline mode, it's the Modern POS machine itself.</span></span> <span data-ttu-id="35b14-118">パッケージを取得するには、[Visual C++ 再頒布可能パッケージをダウンロード](https://www.microsoft.com/download/details.aspx?id=48145)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35b14-118">To get the packages, see [Download the Visual C++ Redistributable Packages](https://www.microsoft.com/download/details.aspx?id=48145).</span></span>

## <a name="development-environment"></a><span data-ttu-id="35b14-119">開発環境</span><span class="sxs-lookup"><span data-stu-id="35b14-119">Development environment</span></span>

<span data-ttu-id="35b14-120">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="35b14-120">Follow these steps to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="35b14-121">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="35b14-121">The CRT extension components</span></span>

<span data-ttu-id="35b14-122">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="35b14-122">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="35b14-123">次の手順を完了するには、CRT ソリューション **CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="35b14-123">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**.</span></span> <span data-ttu-id="35b14-124">このソリューションは **RetailSdk\\SampleExtensions\\CommerceRuntime** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-124">You can find this solution under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="35b14-125">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-125">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

1. <span data-ttu-id="35b14-126">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="35b14-126">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="35b14-127">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="35b14-127">Find the following files:</span></span>

    - <span data-ttu-id="35b14-128">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-128">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="35b14-129">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-129">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="35b14-130">**Reference\\Newtonsoft.Json\\9.0.0.0** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-130">In the **Reference\\Newtonsoft.Json\\9.0.0.0** folder:</span></span>

        - <span data-ttu-id="35b14-131">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-131">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="35b14-132">**Reference\\TaxEngine** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-132">In the **Reference\\TaxEngine** folder:</span></span>

        - <span data-ttu-id="35b14-133">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-133">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="35b14-134">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-134">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="35b14-135">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-135">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="35b14-136">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-136">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="35b14-137">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-137">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>
        - <span data-ttu-id="35b14-138">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-138">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="35b14-139">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-139">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="35b14-140">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-140">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="35b14-141">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-141">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="35b14-142">以下のフォルダーを **Reference\\Z3** フォルダー内で見つけます:</span><span class="sxs-lookup"><span data-stu-id="35b14-142">Find the following folders in the **Reference\\Z3** folder:</span></span>

        - <span data-ttu-id="35b14-143">x86</span><span class="sxs-lookup"><span data-stu-id="35b14-143">x86</span></span>
        - <span data-ttu-id="35b14-144">x64</span><span class="sxs-lookup"><span data-stu-id="35b14-144">x64</span></span>

3. <span data-ttu-id="35b14-145">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="35b14-145">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="35b14-146">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="35b14-146">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="35b14-147">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="35b14-147">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="35b14-148">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="35b14-148">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="35b14-149">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-149">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="35b14-150">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-150">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="35b14-151">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="35b14-151">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="35b14-152">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="35b14-152">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="35b14-153">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="35b14-153">These files aren't intended for any customizations.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-154">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-154">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

1. <span data-ttu-id="35b14-155">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="35b14-155">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="35b14-156">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="35b14-156">Find the following files:</span></span>

    - <span data-ttu-id="35b14-157">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-157">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="35b14-158">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-158">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="35b14-159">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-159">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="35b14-160">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-160">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="35b14-161">**References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-161">In the **References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="35b14-162">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-162">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="35b14-163">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-163">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="35b14-164">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-164">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="35b14-165">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-165">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="35b14-166">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-166">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="35b14-167">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-167">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="35b14-168">**References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-168">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="35b14-169">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-169">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="35b14-170">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-170">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="35b14-171">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-171">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="35b14-172">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="35b14-172">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="35b14-173">x86</span><span class="sxs-lookup"><span data-stu-id="35b14-173">x86</span></span>
        - <span data-ttu-id="35b14-174">x64</span><span class="sxs-lookup"><span data-stu-id="35b14-174">x64</span></span>

3. <span data-ttu-id="35b14-175">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="35b14-175">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="35b14-176">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="35b14-176">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="35b14-177">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="35b14-177">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="35b14-178">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="35b14-178">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="35b14-179">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-179">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="35b14-180">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-180">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="35b14-181">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="35b14-181">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="35b14-182">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="35b14-182">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="35b14-183">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="35b14-183">These files aren't intended for any customizations.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-184">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-184">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

1. <span data-ttu-id="35b14-185">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="35b14-185">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="35b14-186">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="35b14-186">Find the following files:</span></span>

    - <span data-ttu-id="35b14-187">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-187">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="35b14-188">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-188">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="35b14-189">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-189">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="35b14-190">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-190">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="35b14-191">**References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-191">In the **References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="35b14-192">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-192">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="35b14-193">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-193">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="35b14-194">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-194">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="35b14-195">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-195">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="35b14-196">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-196">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="35b14-197">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-197">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="35b14-198">**References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="35b14-198">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="35b14-199">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-199">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="35b14-200">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-200">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="35b14-201">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="35b14-201">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="35b14-202">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="35b14-202">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="35b14-203">x86</span><span class="sxs-lookup"><span data-stu-id="35b14-203">x86</span></span>
        - <span data-ttu-id="35b14-204">x64</span><span class="sxs-lookup"><span data-stu-id="35b14-204">x64</span></span>

3. <span data-ttu-id="35b14-205">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="35b14-205">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="35b14-206">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="35b14-206">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="35b14-207">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="35b14-207">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="35b14-208">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="35b14-208">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="35b14-209">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-209">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="35b14-210">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-210">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="35b14-211">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="35b14-211">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="35b14-212">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="35b14-212">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="35b14-213">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="35b14-213">These files aren't intended for any customizations.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-214">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-214">Retail 10.0 and later</span></span>](#tab/retail-10-0)

<span data-ttu-id="35b14-215">汎用税エンジン コンポーネントはシールド拡張機能の一部です。</span><span class="sxs-lookup"><span data-stu-id="35b14-215">The Generic Tax Engine component is a part of sealed extensions.</span></span>

1. <span data-ttu-id="35b14-216">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="35b14-216">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="35b14-217">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-217">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="35b14-218">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-218">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="35b14-219">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="35b14-219">Register the CRT change in the extensions configuration file:</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="35b14-220">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては *いけません*。</span><span class="sxs-lookup"><span data-stu-id="35b14-220">Do *not* edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="35b14-221">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="35b14-221">These files aren't intended for any customizations.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-222">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-222">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="35b14-223">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="35b14-223">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="35b14-224">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-224">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="35b14-225">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="35b14-225">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="35b14-226">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="35b14-226">Register the CRT change in the extensions configuration file:</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="35b14-227">上に示すように、拡張機能の順序を保持します。</span><span class="sxs-lookup"><span data-stu-id="35b14-227">Keep the order of the extensions as shown above.</span></span>

    > [!WARNING]
    > <span data-ttu-id="35b14-228">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="35b14-228">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="35b14-229">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="35b14-229">These files aren't intended for any customizations.</span></span>

---

### <a name="the-extension-components"></a><span data-ttu-id="35b14-230">拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="35b14-230">The extension components</span></span>

1. <span data-ttu-id="35b14-231">IIS Retail Server サイトがある場所の下にあるルート フォルダーの **web.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="35b14-231">Open **web.config** in the root folder under the IIS Retail Server site location.</span></span> <span data-ttu-id="35b14-232">Retail Server はコマース 10.0.8 およびそれ以降では Commerce Scale Unit と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="35b14-232">Note that Retail Server is known as Commerce Scale Unit in Commerce 10.0.8 and above.</span></span>
2. <span data-ttu-id="35b14-233">コンフィギュレーション ファイルの **extensionComposition** セクションで拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="35b14-233">Register the extensions in the **extensionComposition** section of the configuration file.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="35b14-234">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-234">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="35b14-235">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-235">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-236">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-236">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="35b14-237">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-237">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-238">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-238">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="35b14-239">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-239">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-240">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-240">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="35b14-241">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-241">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-242">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-242">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

``` xml
<add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
```

---
### <a name="the-clientbroker-extension-components"></a><span data-ttu-id="35b14-243">ClientBroker 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="35b14-243">The ClientBroker extension components</span></span>

1. <span data-ttu-id="35b14-244">ローカル CRT クライアント ブローカーの場所の下にある **RetailProxy.MPOSOffline.ext.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="35b14-244">Open **RetailProxy.MPOSOffline.ext.config** under the local CRT client broker location.</span></span>
2. <span data-ttu-id="35b14-245">コンフィギュレーション ファイルの **extensionComposition** セクションで、プロキシ拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="35b14-245">Register the Proxy extensions in the **extensionComposition** section of the configuration file.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="35b14-246">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-246">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="35b14-247">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-247">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-248">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-248">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="35b14-249">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-249">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-250">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-250">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="35b14-251">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-251">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-252">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-252">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="35b14-253">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-253">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-254">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-254">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

``` xml
<add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
```

---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="35b14-255">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="35b14-255">The Modern POS extension components</span></span>

<span data-ttu-id="35b14-256">税登録の ID 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="35b14-256">Enable the Tax Registration Id extension.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="35b14-257">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-257">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="35b14-258">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-258">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-259">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-259">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="35b14-260">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-260">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-261">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-261">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="35b14-262">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-262">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-263">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-263">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="35b14-264">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-264">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-265">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-265">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="35b14-266">**RetailSdk\POS\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="35b14-266">Open the solution at **RetailSdk\POS\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="35b14-267">また、Modern POS が Run コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="35b14-267">Also make sure that Modern POS can be run from Microsoft Visual Studio using the Run command.</span></span> <span data-ttu-id="35b14-268">(Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="35b14-268">(Modern POS must not be customized.</span></span> <span data-ttu-id="35b14-269">ユーザー アカウント制御 [UAC] を有効にして、以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。)</span><span class="sxs-lookup"><span data-stu-id="35b14-269">You must enable User Account Control [UAC], and uninstall previously installed instances of Modern POS.)</span></span>

2. <span data-ttu-id="35b14-270">**POS.Extensions\extensions.json** で、次の行を追加することによって拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="35b14-270">Enable the extension in **POS.Extensions\extensions.json** by adding the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. <span data-ttu-id="35b14-271">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="35b14-271">Build the solution.</span></span>
4. <span data-ttu-id="35b14-272">Modern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="35b14-272">Run Modern POS and test the functionality.</span></span>

---

### <a name="the-cloud-pos-extension-components"></a><span data-ttu-id="35b14-273">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="35b14-273">The Cloud POS extension components</span></span>

<span data-ttu-id="35b14-274">税登録の ID 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="35b14-274">Enable the Tax Registration Id extension.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="35b14-275">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-275">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="35b14-276">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-276">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-277">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-277">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="35b14-278">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-278">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-279">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-279">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="35b14-280">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-280">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-281">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-281">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="35b14-282">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-282">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-283">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-283">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="35b14-284">**RetailSdk\POS\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="35b14-284">Open the solution at **RetailSdk\POS\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="35b14-285">**POS.Extensions\extensions.json** で、次の行を追加することによって拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="35b14-285">Enable the extension in **POS.Extensions\extensions.json** by adding the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. <span data-ttu-id="35b14-286">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="35b14-286">Build the solution.</span></span>
4. <span data-ttu-id="35b14-287">クラウド POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="35b14-287">Run Cloud POS and test the functionality.</span></span>

---

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="35b14-288">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="35b14-288">Set up required parameters in Headquarters</span></span>

<span data-ttu-id="35b14-289">詳細については、[インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合](./apac-ind-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35b14-289">For more information, see [Goods and Services Tax (GST) integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="35b14-290">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="35b14-290">Production environment</span></span>

<span data-ttu-id="35b14-291">以下の手順に従い、コンポーネントを含む配置可能パッケージを作成して、パッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="35b14-291">Follow these steps to create deployable packages that contain components, and to apply the packages in a production environment.</span></span>

1. <span data-ttu-id="35b14-292">**RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-292">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files under the **RetailSdk\\Assets** folder, add the following lines to the **composition** section.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="35b14-293">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-293">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-294">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-294">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-295">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-295">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-296">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-296">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-297">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-297">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="35b14-298">上に示すように、拡張機能の順序を保持します。</span><span class="sxs-lookup"><span data-stu-id="35b14-298">Keep the order of the extensions as shown above.</span></span>

    ---

2. <span data-ttu-id="35b14-299">**RetailSdk\\Assets** フォルダーの下の **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-299">In the **RetailProxy.MPOSOffline.ext.config** configuration file under the **RetailSdk\\Assets** folder, add the following lines to the **composition** section.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="35b14-300">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-300">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="35b14-301">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-301">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-302">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-302">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="35b14-303">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-303">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-304">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-304">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="35b14-305">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-305">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-306">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-306">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="35b14-307">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-307">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-308">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-308">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
    ```

    ---

3. <span data-ttu-id="35b14-309">Web のコンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="35b14-309">Update the web configuration file.</span></span> <span data-ttu-id="35b14-310">**RetailSDK\Packages\RetailServer\Code\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-310">In the **RetailSDK\Packages\RetailServer\Code\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="35b14-311">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-311">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="35b14-312">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-312">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-313">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-313">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="35b14-314">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-314">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-315">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-315">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="35b14-316">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-316">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-317">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-317">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="35b14-318">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-318">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-319">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-319">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
    ```

    ---

4. <span data-ttu-id="35b14-320">**RetailSdk\\BuildTools** フォルダーの下の **Customization.settings** パッケージ カスタマイズ構成ファイルで、以下の行を **ItemGroup** セクションに追加して、配置可能パッケージ内の CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="35b14-320">In the **Customization.settings** package customization configuration file under the **RetailSdk\\BuildTools** folder, add the following lines to the **ItemGroup** section to include the CRT extensions in deployable packages.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="35b14-321">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-321">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

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

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-322">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-322">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-323">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-323">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

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

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-324">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-324">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="35b14-325">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-325">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-326">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-326">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    > [!NOTE]
    > <span data-ttu-id="35b14-327">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-327">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="35b14-328">以下のファイルを修正して、配置可能パッケージに Z3 ライブラリを含めます。</span><span class="sxs-lookup"><span data-stu-id="35b14-328">Modify the following files to include the Z3 libraries in deployable packages:</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="35b14-329">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-329">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="35b14-330">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="35b14-330">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="35b14-331">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="35b14-331">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="35b14-332">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="35b14-332">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="35b14-333">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-333">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="..\..\References\Z3\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="..\..\References\Z3\x64\*.*" />
    ```

    <span data-ttu-id="35b14-334">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-334">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="35b14-335">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-335">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>
    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-336">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-336">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="35b14-337">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="35b14-337">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="35b14-338">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="35b14-338">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="35b14-339">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="35b14-339">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="35b14-340">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-340">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
    ```

    <span data-ttu-id="35b14-341">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-341">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="35b14-342">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-342">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-343">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-343">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    - <span data-ttu-id="35b14-344">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span><span class="sxs-lookup"><span data-stu-id="35b14-344">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span></span>
    - <span data-ttu-id="35b14-345">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="35b14-345">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="35b14-346">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-346">Add the following lines to the **ItemGroup** section.</span></span>

     ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
     ```

    <span data-ttu-id="35b14-347">**Sdk.ModernPos.Shared.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-347">For **Sdk.ModernPos.Shared.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="35b14-348">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-348">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-349">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-349">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="35b14-350">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-350">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-351">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-351">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    > [!NOTE]
    > <span data-ttu-id="35b14-352">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-352">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="35b14-353">税登録の ID POS 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="35b14-353">Enable the Tax Registration Id POS extension:</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="35b14-354">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="35b14-354">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="35b14-355">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-355">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="35b14-356">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-356">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="35b14-357">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-357">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="35b14-358">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-358">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="35b14-359">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-359">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="35b14-360">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-360">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="35b14-361">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="35b14-361">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="35b14-362">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="35b14-362">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    <span data-ttu-id="35b14-363">**RetailSDK\POS\Extensions\extensions.json** を開いて、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="35b14-363">Open **RetailSDK\POS\Extensions\extensions.json** and add the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

7. <span data-ttu-id="35b14-364">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="35b14-364">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
8. <span data-ttu-id="35b14-365">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="35b14-365">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="35b14-366">詳細については、 [小売の配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35b14-366">For more information, see [Create retail deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>
