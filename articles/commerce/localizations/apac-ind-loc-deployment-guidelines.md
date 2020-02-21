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
ms.search.scope: Retail
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: fe9a676bd15d16cd0391fcc1a4f3ea33edc28dd5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004684"
---
# <a name="deployment-guidelines-for-cash-registers-for-india"></a><span data-ttu-id="06a59-103">インドのキャッシュ レジスターの配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="06a59-103">Deployment guidelines for cash registers for India</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06a59-104">このトピックは、インドの Dynamics 365 Commerce アプリのローカライズで商品及びサービス税 (GST) の要件を有効にする方法を示す配置ガイドです。</span><span class="sxs-lookup"><span data-stu-id="06a59-104">This topic is a deployment guide that shows how to enable the requirements for Goods and Services Tax (GST) in the Dynamics 365 Commerce app's localization for India.</span></span> <span data-ttu-id="06a59-105">インドのローカライズの詳細については、[インド向けのキャッシュ レジスターの商品及びサービス税 (GST) 統合](./apac-ind-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06a59-105">For more information about the localization for India, see [Goods and Services Tax (GST) integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

<span data-ttu-id="06a59-106">このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="06a59-106">This sample is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="06a59-107">SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06a59-107">For information about how to install and use the SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="06a59-108">このサンプルは Commerce runtime (CRT) の拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="06a59-108">This sample consists of extensions for the Commerce runtime (CRT).</span></span> <span data-ttu-id="06a59-109">このサンプルを実行するには、CRT プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06a59-109">To run this sample, you must modify and build the CRT projects.</span></span> <span data-ttu-id="06a59-110">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="06a59-110">We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="06a59-111">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="06a59-111">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="06a59-112">使用しているアプリのバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="06a59-112">Some steps in the procedures in this topic differ, depending on the version of the app that you're using.</span></span> <span data-ttu-id="06a59-113">詳細については、 [Dynamics 365 Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06a59-113">For more information, see [What's new or changed in Dynamics 365 Retail](../get-started/whats-new.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="06a59-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="06a59-114">Prerequisites</span></span>

<span data-ttu-id="06a59-115">Visual C++ 再頒布可能パッケージが商品及びサービス税 (GST) 計算を実行するマシン上にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="06a59-115">Make sure that the Visual C++ Redistributable Packages are present on the machine that you're running Goods and Services Tax (GST) calculations on.</span></span> <span data-ttu-id="06a59-116">クラウド POS、およびオンライン モードの Modern POS の場合は、このマシンは小売サーバーとなります (小売サーバーは、コマース 10.0.8 とそれ以降で Commerce Scale Unit と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="06a59-116">For Cloud POS, and for Modern POS in online mode, this machine is Retail Server (Retail Server is known as Commerce Scale Unit in Commerce 10.0.8 and above).</span></span> <span data-ttu-id="06a59-117">オフライン モードの Modern POS の場合、それは Modern POS マシン自身です。</span><span class="sxs-lookup"><span data-stu-id="06a59-117">For Modern POS in offline mode, it's the Modern POS machine itself.</span></span> <span data-ttu-id="06a59-118">パッケージを取得するには、[Visual C++ 再頒布可能パッケージをダウンロード](https://www.microsoft.com/download/details.aspx?id=48145)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06a59-118">To get the packages, see [Download the Visual C++ Redistributable Packages](https://www.microsoft.com/download/details.aspx?id=48145).</span></span>

## <a name="development-environment"></a><span data-ttu-id="06a59-119">開発環境</span><span class="sxs-lookup"><span data-stu-id="06a59-119">Development environment</span></span>

<span data-ttu-id="06a59-120">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06a59-120">Follow these steps to set up a development environment so that you can test and extend the sample.</span></span>

### <a name="the-crt-extension-components"></a><span data-ttu-id="06a59-121">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="06a59-121">The CRT extension components</span></span>

<span data-ttu-id="06a59-122">CRT サンプルには、CRT 拡張コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="06a59-122">The CRT extension components are included in the CRT samples.</span></span> <span data-ttu-id="06a59-123">次の手順を完了するには、CRT ソリューション **CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="06a59-123">To complete the following procedures, open the CRT solution, **CommerceRuntimeSamples.sln**.</span></span> <span data-ttu-id="06a59-124">このソリューションは **RetailSdk\\SampleExtensions\\CommerceRuntime** の下にあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-124">You can find this solution under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="06a59-125">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-125">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

1. <span data-ttu-id="06a59-126">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="06a59-126">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="06a59-127">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="06a59-127">Find the following files:</span></span>

    - <span data-ttu-id="06a59-128">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-128">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="06a59-129">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-129">Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="06a59-130">**Reference\\Newtonsoft.Json\\9.0.0.0** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-130">In the **Reference\\Newtonsoft.Json\\9.0.0.0** folder:</span></span>

        - <span data-ttu-id="06a59-131">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-131">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="06a59-132">**Reference\\TaxEngine** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-132">In the **Reference\\TaxEngine** folder:</span></span>

        - <span data-ttu-id="06a59-133">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-133">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="06a59-134">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-134">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="06a59-135">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-135">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="06a59-136">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-136">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="06a59-137">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-137">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>
        - <span data-ttu-id="06a59-138">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-138">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="06a59-139">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-139">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="06a59-140">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-140">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="06a59-141">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-141">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="06a59-142">以下のフォルダーを **Reference\\Z3** フォルダー内で見つけます:</span><span class="sxs-lookup"><span data-stu-id="06a59-142">Find the following folders in the **Reference\\Z3** folder:</span></span>

        - <span data-ttu-id="06a59-143">x86</span><span class="sxs-lookup"><span data-stu-id="06a59-143">x86</span></span>
        - <span data-ttu-id="06a59-144">x64</span><span class="sxs-lookup"><span data-stu-id="06a59-144">x64</span></span>

3. <span data-ttu-id="06a59-145">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="06a59-145">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="06a59-146">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="06a59-146">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="06a59-147">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="06a59-147">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="06a59-148">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="06a59-148">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="06a59-149">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-149">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="06a59-150">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-150">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="06a59-151">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="06a59-151">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="06a59-152">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="06a59-152">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="06a59-153">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="06a59-153">These files aren't intended for any customizations.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-154">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-154">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

1. <span data-ttu-id="06a59-155">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="06a59-155">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="06a59-156">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="06a59-156">Find the following files:</span></span>

    - <span data-ttu-id="06a59-157">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-157">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="06a59-158">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-158">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="06a59-159">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-159">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="06a59-160">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-160">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="06a59-161">**References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-161">In the **References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="06a59-162">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-162">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="06a59-163">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-163">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="06a59-164">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-164">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="06a59-165">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-165">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="06a59-166">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-166">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="06a59-167">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-167">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="06a59-168">**References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-168">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="06a59-169">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-169">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="06a59-170">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-170">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="06a59-171">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-171">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="06a59-172">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="06a59-172">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="06a59-173">x86</span><span class="sxs-lookup"><span data-stu-id="06a59-173">x86</span></span>
        - <span data-ttu-id="06a59-174">x64</span><span class="sxs-lookup"><span data-stu-id="06a59-174">x64</span></span>

3. <span data-ttu-id="06a59-175">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="06a59-175">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="06a59-176">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="06a59-176">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="06a59-177">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="06a59-177">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="06a59-178">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="06a59-178">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="06a59-179">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-179">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="06a59-180">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-180">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="06a59-181">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="06a59-181">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="06a59-182">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="06a59-182">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="06a59-183">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="06a59-183">These files aren't intended for any customizations.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-184">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-184">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

1. <span data-ttu-id="06a59-185">**Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="06a59-185">Find the **Runtime.Extensions.GenericTaxEngine** project, and build it.</span></span>
2. <span data-ttu-id="06a59-186">以下のファイルを検索します:</span><span class="sxs-lookup"><span data-stu-id="06a59-186">Find the following files:</span></span>

    - <span data-ttu-id="06a59-187">**Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-187">In the **Extensions.GenericTaxEngine\\bin\\Debug** folder:</span></span>

        - <span data-ttu-id="06a59-188">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-188">Contoso.Commerce.Runtime.GenericTaxEngine.dll</span></span>

    - <span data-ttu-id="06a59-189">**References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-189">In the **References\\Newtonsoft.Json.9.0.1\\lib\\net45** folder:</span></span>

        - <span data-ttu-id="06a59-190">Newtonsoft.Json.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-190">Newtonsoft.Json.dll</span></span>

    - <span data-ttu-id="06a59-191">**References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-191">In the **References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** folder:</span></span>

        - <span data-ttu-id="06a59-192">Microsoft.Dynamics365.LocalizationFramework.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-192">Microsoft.Dynamics365.LocalizationFramework.dll</span></span>
        - <span data-ttu-id="06a59-193">Microsoft.Dynamics365.Tax.Core.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-193">Microsoft.Dynamics365.Tax.Core.dll</span></span>
        - <span data-ttu-id="06a59-194">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-194">Microsoft.Dynamics365.Tax.DataAccessFramework.dll</span></span>
        - <span data-ttu-id="06a59-195">Microsoft.Dynamics365.Tax.DataAccessor.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-195">Microsoft.Dynamics365.Tax.DataAccessor.dll</span></span>
        - <span data-ttu-id="06a59-196">Microsoft.Dynamics365.Tax.DataModel.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-196">Microsoft.Dynamics365.Tax.DataModel.dll</span></span>
        - <span data-ttu-id="06a59-197">Microsoft.Dynamics365.Tax.Metadata.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-197">Microsoft.Dynamics365.Tax.Metadata.dll</span></span>

    - <span data-ttu-id="06a59-198">**References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** フォルダー内:</span><span class="sxs-lookup"><span data-stu-id="06a59-198">In the **References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** folder:</span></span>

        - <span data-ttu-id="06a59-199">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-199">Microsoft.Dynamics365.ElectronicReportingMapping.dll</span></span>
        - <span data-ttu-id="06a59-200">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-200">Microsoft.Dynamics365.LocalizationFrameworkCore.dll</span></span>
        - <span data-ttu-id="06a59-201">Microsoft.Dynamics365.XppSupportLayer.dll</span><span class="sxs-lookup"><span data-stu-id="06a59-201">Microsoft.Dynamics365.XppSupportLayer.dll</span></span>

    - <span data-ttu-id="06a59-202">以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:</span><span class="sxs-lookup"><span data-stu-id="06a59-202">Find the following folders in the **References\\Z3.4.5.0\\lib\\net40** folder:</span></span>

        - <span data-ttu-id="06a59-203">x86</span><span class="sxs-lookup"><span data-stu-id="06a59-203">x86</span></span>
        - <span data-ttu-id="06a59-204">x64</span><span class="sxs-lookup"><span data-stu-id="06a59-204">x64</span></span>

3. <span data-ttu-id="06a59-205">11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:</span><span class="sxs-lookup"><span data-stu-id="06a59-205">Copy the 11 assembly files, and both x64 and x86 folders to the CRT extensions folder:</span></span>

    - <span data-ttu-id="06a59-206">**小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="06a59-206">**Retail Server:** Copy the assemblies to the **\\bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="06a59-207">**Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="06a59-207">**Local CRT on Modern POS:** Copy the assemblies to the **\\ext** folder under the local CRT client broker location.</span></span>

4. <span data-ttu-id="06a59-208">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="06a59-208">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="06a59-209">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-209">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Retail server site location.</span></span>
    - <span data-ttu-id="06a59-210">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-210">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

5. <span data-ttu-id="06a59-211">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="06a59-211">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="06a59-212">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="06a59-212">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="06a59-213">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="06a59-213">These files aren't intended for any customizations.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-214">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-214">Retail 10.0 and later</span></span>](#tab/retail-10-0)

<span data-ttu-id="06a59-215">汎用税エンジン コンポーネントはシールド拡張機能の一部です。</span><span class="sxs-lookup"><span data-stu-id="06a59-215">The Generic Tax Engine component is a part of sealed extensions.</span></span>

1. <span data-ttu-id="06a59-216">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="06a59-216">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="06a59-217">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-217">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="06a59-218">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-218">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="06a59-219">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="06a59-219">Register the CRT change in the extensions configuration file:</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > <span data-ttu-id="06a59-220">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては*いけません*。</span><span class="sxs-lookup"><span data-stu-id="06a59-220">Do *not* edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="06a59-221">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="06a59-221">These files aren't intended for any customizations.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-222">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-222">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="06a59-223">CRT の拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="06a59-223">Find the extensions configuration file for CRT:</span></span>

    - <span data-ttu-id="06a59-224">**小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-224">**Retail Server:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the Microsoft Internet Information Services (IIS) Retail server site location.</span></span>
    - <span data-ttu-id="06a59-225">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。</span><span class="sxs-lookup"><span data-stu-id="06a59-225">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.</span></span>

2. <span data-ttu-id="06a59-226">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="06a59-226">Register the CRT change in the extensions configuration file:</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="06a59-227">上に示すように、拡張機能の順序を保持します。</span><span class="sxs-lookup"><span data-stu-id="06a59-227">Keep the order of the extensions as shown above.</span></span>

    > [!WARNING]
    > <span data-ttu-id="06a59-228">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="06a59-228">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="06a59-229">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="06a59-229">These files aren't intended for any customizations.</span></span>

---

### <a name="the-extension-components"></a><span data-ttu-id="06a59-230">拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="06a59-230">The extension components</span></span>

1. <span data-ttu-id="06a59-231">IIS Retail Server サイトがある場所の下にあるルート フォルダーの **web.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="06a59-231">Open **web.config** in the root folder under the IIS Retail Server site location.</span></span> <span data-ttu-id="06a59-232">Retail Server はコマース 10.0.8 およびそれ以降では Commerce Scale Unit と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="06a59-232">Note that Retail Server is known as Commerce Scale Unit in Commerce 10.0.8 and above.</span></span>
2. <span data-ttu-id="06a59-233">コンフィギュレーション ファイルの **extensionComposition** セクションで拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="06a59-233">Register the extensions in the **extensionComposition** section of the configuration file.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="06a59-234">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-234">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="06a59-235">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-235">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-236">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-236">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="06a59-237">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-237">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-238">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-238">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="06a59-239">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-239">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-240">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-240">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="06a59-241">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-241">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-242">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-242">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

``` xml
<add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
```

---
### <a name="the-clientbroker-extension-components"></a><span data-ttu-id="06a59-243">ClientBroker 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="06a59-243">The ClientBroker extension components</span></span>

1. <span data-ttu-id="06a59-244">ローカル CRT クライアント ブローカーの場所の下にある **RetailProxy.MPOSOffline.ext.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="06a59-244">Open **RetailProxy.MPOSOffline.ext.config** under the local CRT client broker location.</span></span>
2. <span data-ttu-id="06a59-245">コンフィギュレーション ファイルの **extensionComposition** セクションで、プロキシ拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="06a59-245">Register the Proxy extensions in the **extensionComposition** section of the configuration file.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="06a59-246">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-246">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="06a59-247">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-247">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-248">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-248">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="06a59-249">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-249">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-250">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-250">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="06a59-251">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-251">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-252">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-252">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="06a59-253">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-253">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-254">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-254">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

``` xml
<add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
```

---

### <a name="the-modern-pos-extension-components"></a><span data-ttu-id="06a59-255">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="06a59-255">The Modern POS extension components</span></span>

<span data-ttu-id="06a59-256">税登録の ID 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="06a59-256">Enable the Tax Registration Id extension.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="06a59-257">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-257">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="06a59-258">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-258">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-259">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-259">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="06a59-260">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-260">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-261">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-261">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="06a59-262">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-262">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-263">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-263">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="06a59-264">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-264">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-265">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-265">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="06a59-266">**RetailSdk\POS\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="06a59-266">Open the solution at **RetailSdk\POS\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="06a59-267">また、Modern POS が Run コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="06a59-267">Also make sure that Modern POS can be run from Microsoft Visual Studio using the Run command.</span></span> <span data-ttu-id="06a59-268">(Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="06a59-268">(Modern POS must not be customized.</span></span> <span data-ttu-id="06a59-269">ユーザー アカウント制御 [UAC] を有効にして、以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。)</span><span class="sxs-lookup"><span data-stu-id="06a59-269">You must enable User Account Control [UAC], and uninstall previously installed instances of Modern POS.)</span></span>

2. <span data-ttu-id="06a59-270">**POS.Extensions\extensions.json** で、次の行を追加することによって拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="06a59-270">Enable the extension in **POS.Extensions\extensions.json** by adding the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. <span data-ttu-id="06a59-271">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="06a59-271">Build the solution.</span></span>
4. <span data-ttu-id="06a59-272">Modern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="06a59-272">Run Modern POS and test the functionality.</span></span>

---

### <a name="the-cloud-pos-extension-components"></a><span data-ttu-id="06a59-273">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="06a59-273">The Cloud POS extension components</span></span>

<span data-ttu-id="06a59-274">税登録の ID 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="06a59-274">Enable the Tax Registration Id extension.</span></span>

# <a name="retail-731"></a>[<span data-ttu-id="06a59-275">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-275">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

> [!NOTE]
> <span data-ttu-id="06a59-276">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-276">This step doesn't apply to this version.</span></span>

# <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-277">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-277">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

> [!NOTE]
> <span data-ttu-id="06a59-278">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-278">This step doesn't apply to this version.</span></span>

# <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-279">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-279">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

> [!NOTE]
> <span data-ttu-id="06a59-280">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-280">This step doesn't apply to this version.</span></span>

# <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-281">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-281">Retail 10.0 and later</span></span>](#tab/retail-10-0)

> [!NOTE]
> <span data-ttu-id="06a59-282">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-282">This step doesn't apply to this version.</span></span>

# <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-283">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-283">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

1. <span data-ttu-id="06a59-284">**RetailSdk\POS\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="06a59-284">Open the solution at **RetailSdk\POS\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="06a59-285">**POS.Extensions\extensions.json** で、次の行を追加することによって拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="06a59-285">Enable the extension in **POS.Extensions\extensions.json** by adding the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. <span data-ttu-id="06a59-286">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="06a59-286">Build the solution.</span></span>
4. <span data-ttu-id="06a59-287">クラウド POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="06a59-287">Run Cloud POS and test the functionality.</span></span>

---

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="06a59-288">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="06a59-288">Set up required parameters in Headquarters</span></span>

<span data-ttu-id="06a59-289">詳細については、[インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合](./apac-ind-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06a59-289">For more information, see [Goods and Services Tax (GST) integration for cash registers for India](./apac-ind-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="06a59-290">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="06a59-290">Production environment</span></span>

<span data-ttu-id="06a59-291">以下の手順に従い、コンポーネントを含む配置可能パッケージを作成して、パッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="06a59-291">Follow these steps to create deployable packages that contain components, and to apply the packages in a production environment.</span></span>

1. <span data-ttu-id="06a59-292">**RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-292">In the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** configuration files under the **RetailSdk\\Assets** folder, add the following lines to the **composition** section.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="06a59-293">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-293">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-294">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-294">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-295">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-295">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-296">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-296">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-297">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-297">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="06a59-298">上に示すように、拡張機能の順序を保持します。</span><span class="sxs-lookup"><span data-stu-id="06a59-298">Keep the order of the extensions as shown above.</span></span>

    ---

2. <span data-ttu-id="06a59-299">**RetailSdk\\Assets** フォルダーの下の **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、以下の行を**合成**セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-299">In the **RetailProxy.MPOSOffline.ext.config** configuration file under the **RetailSdk\\Assets** folder, add the following lines to the **composition** section.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="06a59-300">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-300">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="06a59-301">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-301">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-302">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-302">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="06a59-303">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-303">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-304">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-304">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="06a59-305">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-305">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-306">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-306">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="06a59-307">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-307">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-308">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-308">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
    ```

    ---

3. <span data-ttu-id="06a59-309">Web のコンフィギュレーション ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="06a59-309">Update the web configuration file.</span></span> <span data-ttu-id="06a59-310">**RetailSDK\Packages\RetailServer\Code\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-310">In the **RetailSDK\Packages\RetailServer\Code\web.config** file, add the following lines to the **extensionComposition** section.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="06a59-311">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-311">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="06a59-312">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-312">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-313">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-313">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="06a59-314">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-314">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-315">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-315">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="06a59-316">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-316">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-317">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-317">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="06a59-318">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-318">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-319">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-319">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
    ```

    ---

4. <span data-ttu-id="06a59-320">**RetailSdk\\BuildTools** フォルダーの下の **Customization.settings** パッケージ カスタマイズ構成ファイルで、以下の行を **ItemGroup** セクションに追加して、配置可能パッケージ内の CRT 拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="06a59-320">In the **Customization.settings** package customization configuration file under the **RetailSdk\\BuildTools** folder, add the following lines to the **ItemGroup** section to include the CRT extensions in deployable packages.</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="06a59-321">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-321">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

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

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-322">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-322">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

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

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-323">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-323">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

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

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-324">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-324">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="06a59-325">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-325">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-326">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-326">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    > [!NOTE]
    > <span data-ttu-id="06a59-327">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-327">This step doesn't apply to this version.</span></span>

    ---

5. <span data-ttu-id="06a59-328">以下のファイルを修正して、配置可能パッケージに Z3 ライブラリを含めます。</span><span class="sxs-lookup"><span data-stu-id="06a59-328">Modify the following files to include the Z3 libraries in deployable packages:</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="06a59-329">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-329">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    - <span data-ttu-id="06a59-330">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="06a59-330">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="06a59-331">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="06a59-331">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="06a59-332">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="06a59-332">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="06a59-333">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-333">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="..\..\References\Z3\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="..\..\References\Z3\x64\*.*" />
    ```

    <span data-ttu-id="06a59-334">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-334">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="06a59-335">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-335">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>
    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-336">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-336">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    - <span data-ttu-id="06a59-337">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span><span class="sxs-lookup"><span data-stu-id="06a59-337">Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj</span></span>
    - <span data-ttu-id="06a59-338">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span><span class="sxs-lookup"><span data-stu-id="06a59-338">Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj</span></span>
    - <span data-ttu-id="06a59-339">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="06a59-339">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="06a59-340">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-340">Add the following lines to the **ItemGroup** section.</span></span>

    ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
    ```

    <span data-ttu-id="06a59-341">**Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-341">For **Sdk.ModernPOSSetup.csproj** and **Sdk.ModernPOSSetupOffline.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="06a59-342">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-342">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-343">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-343">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    - <span data-ttu-id="06a59-344">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span><span class="sxs-lookup"><span data-stu-id="06a59-344">Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj</span></span>
    - <span data-ttu-id="06a59-345">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span><span class="sxs-lookup"><span data-stu-id="06a59-345">Packages\\RetailServer\\Sdk.RetailServerSetup.proj</span></span>

    <span data-ttu-id="06a59-346">以下の行を **ItemGroup** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-346">Add the following lines to the **ItemGroup** section.</span></span>

     ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
     ```

    <span data-ttu-id="06a59-347">**Sdk.ModernPos.Shared.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-347">For **Sdk.ModernPos.Shared.csproj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    <span data-ttu-id="06a59-348">**Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-348">For **Sdk.RetailServerSetup.proj** also add the following lines to the **\<Target Name="CopyPackageFiles"\>** section.</span></span>

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-349">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-349">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="06a59-350">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-350">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-351">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-351">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    > [!NOTE]
    > <span data-ttu-id="06a59-352">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-352">This step doesn't apply to this version.</span></span>

    ---

6. <span data-ttu-id="06a59-353">税登録の ID POS 拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="06a59-353">Enable the Tax Registration Id POS extension:</span></span>

    # <a name="retail-731"></a>[<span data-ttu-id="06a59-354">Retail 7.3.1</span><span class="sxs-lookup"><span data-stu-id="06a59-354">Retail 7.3.1</span></span>](#tab/retail-7-3-1)

    > [!NOTE]
    > <span data-ttu-id="06a59-355">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-355">This step doesn't apply to this version.</span></span>

    # <a name="retail-732-and-later"></a>[<span data-ttu-id="06a59-356">Retail 7.3.2 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-356">Retail 7.3.2 and later</span></span>](#tab/retail-7-3-2)

    > [!NOTE]
    > <span data-ttu-id="06a59-357">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-357">This step doesn't apply to this version.</span></span>

    # <a name="retail-813-and-later"></a>[<span data-ttu-id="06a59-358">Retail 8.1.3 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-358">Retail 8.1.3 and later</span></span>](#tab/retail-8-1-3)

    > [!NOTE]
    > <span data-ttu-id="06a59-359">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-359">This step doesn't apply to this version.</span></span>

    # <a name="retail-100-and-later"></a>[<span data-ttu-id="06a59-360">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-360">Retail 10.0 and later</span></span>](#tab/retail-10-0)

    > [!NOTE]
    > <span data-ttu-id="06a59-361">このバージョンには、この手順は適用されません。</span><span class="sxs-lookup"><span data-stu-id="06a59-361">This step doesn't apply to this version.</span></span>

    # <a name="retail-1006-and-later"></a>[<span data-ttu-id="06a59-362">Retail 10.0.6 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="06a59-362">Retail 10.0.6 and later</span></span>](#tab/retail-10-0-6)

    <span data-ttu-id="06a59-363">**RetailSDK\POS\Extensions\extensions.json** を開いて、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="06a59-363">Open **RetailSDK\POS\Extensions\extensions.json** and add the following lines:</span></span>

    ``` xml
    {
      "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

7. <span data-ttu-id="06a59-364">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="06a59-364">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
8. <span data-ttu-id="06a59-365">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="06a59-365">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="06a59-366">詳細については、 [小売の配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06a59-366">For more information, see [Create retail deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>
