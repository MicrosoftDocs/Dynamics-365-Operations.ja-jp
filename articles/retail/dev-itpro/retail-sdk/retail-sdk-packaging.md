---
title: "Retail SDK パッケージ"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の配置可能小売パッケージを作成する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: 0fa3c8e7-49e4-417d-afe9-fa2055f6546f
ms.search.region: Global
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6c6c7c3f63b7a49820811a7ec80248b09b6e3acf
ms.openlocfilehash: 37dfe38c7e7912503133a41ce600f0d3543d6e39
ms.contentlocale: ja-jp
ms.lasthandoff: 06/19/2018

---

# <a name="retail-sdk-packaging"></a><span data-ttu-id="e5532-103">Retail SDK パッケージ</span><span class="sxs-lookup"><span data-stu-id="e5532-103">Retail SDK packaging</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5532-104">このトピックでは、次のような Retail コンポーネントの拡張機能のカスタマイズをパッケージ化し、Microsoft Dynamics Lifecycle Services (LCS) を使用して、パッケージを環境に配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e5532-104">This topic explains how to package customizations for extensions of the following Retail components and deploy the package to your environment by using Microsoft Dynamics Lifecycle Services (LCS):</span></span>

- <span data-ttu-id="e5532-105">Commerce Runtime (CRT)</span><span class="sxs-lookup"><span data-stu-id="e5532-105">Commerce runtime (CRT)</span></span>
- <span data-ttu-id="e5532-106">Retail プロキシ</span><span class="sxs-lookup"><span data-stu-id="e5532-106">Retail proxy</span></span>
- <span data-ttu-id="e5532-107">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="e5532-107">Retail Server</span></span>
- <span data-ttu-id="e5532-108">Modern POS</span><span class="sxs-lookup"><span data-stu-id="e5532-108">Modern POS</span></span>
- <span data-ttu-id="e5532-109">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="e5532-109">Cloud POS</span></span>
- <span data-ttu-id="e5532-110">ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="e5532-110">Hardware station</span></span>
- <span data-ttu-id="e5532-111">チャネル データベース スクリプト</span><span class="sxs-lookup"><span data-stu-id="e5532-111">Channel database scripts</span></span>
- <span data-ttu-id="e5532-112">支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="e5532-112">Payment connector</span></span>
- <span data-ttu-id="e5532-113">Retail Store スケール ユニット</span><span class="sxs-lookup"><span data-stu-id="e5532-113">Retail Store Scale Unit</span></span>
- <span data-ttu-id="e5532-114">ハイブリッド アプリ (IOS および Android POS アプリ)</span><span class="sxs-lookup"><span data-stu-id="e5532-114">Hybrid app (IOS and Android POS app)</span></span>

## <a name="retail-deployable-package"></a><span data-ttu-id="e5532-115">配置可能小売パッケージ</span><span class="sxs-lookup"><span data-stu-id="e5532-115">Retail deployable package</span></span>
<span data-ttu-id="e5532-116">小売可能なパッケージは、配置に必要なすべてのメタデータと共に、すべてのカスタマイズを含む 1 つの結合されたパッケージです。</span><span class="sxs-lookup"><span data-stu-id="e5532-116">A retail deployable package is one combined package that contains all your customizations together with all the metadata that is required for deployment.</span></span> <span data-ttu-id="e5532-117">この小売展開可能パッケージを使用して、カスタマイズをさまざまな環境に展開できます。</span><span class="sxs-lookup"><span data-stu-id="e5532-117">You can use this retail deployable package to deploy your customizations to various environments.</span></span> <span data-ttu-id="e5532-118">LCS で自動フローを使用して、配置を行うことができます。またはパッケージ内に用意されているスクリプトを使用して手動で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e5532-118">You can do the deployment by using the automated flow in LCS, or you can do it manually by using the scripts that are provided inside the package.</span></span> <span data-ttu-id="e5532-119">このトピックでは、配置可能小売パッケージを生成するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="e5532-119">This topic guides you through the process of generating the retail deployable package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5532-120">Retail コンポーネントのすべてのカスタマイズは、1 つの配置可能なパッケージとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="e5532-120">All customizations for the Retail components are packaged as a single retail deployable package.</span></span> <span data-ttu-id="e5532-121">Finance and Operations は、Modern POS、Cloud POS、Retail Store Scale Unit、CRT、Retail Server といった、個々の Retail コンポーネントの個別のパッケージをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e5532-121">Finance and Operations doesn't support separate packages for individual Retail components, such as Modern POS, Cloud POS, Retail Store Scale Unit, CRT, and Retail Server.</span></span> <span data-ttu-id="e5532-122">独立したソフトウェア ベンダー (ISV) またはさまざまなパートナーの拡張機能をマージまたは結合する必要がある場合でも、すべての拡張機能を単一の小売展開可能パッケージとしてパッケージする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5532-122">You must package all extensions as a single retail deployable package, even if you must merge or combine extensions from independent software vendors (ISVs) or various partners.</span></span>
>
> <span data-ttu-id="e5532-123">アプリケーション バージョン 7.1.1541.3036 よりも古い Retail ソフトウェア開発キット (SDK) のバージョンを使用して、カスタマイズが個々の Retail コンポーネント パッケージとして構築されパッケージ化された場合、パッケージは LCS の展開に対してサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="e5532-123">If your customizations were built and packaged as individual Retail component packages by using a version of the Retail software development kit (SDK) that is older than application version 7.1.1541.3036, the packages are no longer supported for deployment in LCS.</span></span> <span data-ttu-id="e5532-124">[KB 4015062](https://fix.lcs.dynamics.com/Home/Index/0/kb/4015062?permission=Download) で修正プログラムを取得する必要があります。その際、カスタマイズはリビルドおよび再梱包されます。</span><span class="sxs-lookup"><span data-stu-id="e5532-124">You must uptake the hotfix in [KB 4015062](https://fix.lcs.dynamics.com/Home/Index/0/kb/4015062?permission=Download), and then rebuild and repackage your customizations.</span></span>

<span data-ttu-id="e5532-125">Retail SDK の詳細情報は、[Retail SDK 概要](retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5532-125">For detailed information about the Retail SDK, see [Retail SDK overview](retail-sdk-overview.md).</span></span>

### <a name="steps-to-create-a-retail-deployable-package"></a><span data-ttu-id="e5532-126">小売展開可能パッケージを作成する手順</span><span class="sxs-lookup"><span data-stu-id="e5532-126">Steps to create a retail deployable package</span></span>
<span data-ttu-id="e5532-127">小売展開可能パッケージを生成するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="e5532-127">There are two ways to generate a retail deployable package.</span></span> <span data-ttu-id="e5532-128">Retail ビルドの自動化を使用することができます。または Retail SDK のビルド ツールを使用し、手動でパッケージを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="e5532-128">You can use the Retail build automation, or you can generate the package manually by using the build tools in the Retail SDK.</span></span> <span data-ttu-id="e5532-129">このトピックでは、手動メソッドを対象としています。</span><span class="sxs-lookup"><span data-stu-id="e5532-129">This topic focuses on the manual method.</span></span>

1. <span data-ttu-id="e5532-130">小売スタックに機能をカスタマイズまたは追加します。</span><span class="sxs-lookup"><span data-stu-id="e5532-130">Customize or add functionality to the Retail stack.</span></span>
2. <span data-ttu-id="e5532-131">ビルド ツールを使用して、カスタマイズされたインストール パッケージを識別して、コードサインし、カスタマイズされた CRT、Retail サーバー、ハードウェア ステーション アセンブリ、カスタマイズされたデータベース スクリプトを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-131">Use the build tools to identify the customized installation package, code-sign it, and specify the customized CRT, Retail Server, and Hardware station assemblies, and customized database scripts.</span></span>
3. <span data-ttu-id="e5532-132">すべての設定が **...\\Retail SDK\\BuildTools** フォルダーの **Customization.settings** ファイルで指定された後、Retail SDK フォルダーのルートで **msbuild /t:rebuild** を起動します。</span><span class="sxs-lookup"><span data-stu-id="e5532-132">After all the settings have been specified in the **Customization.settings** file in the **...\\Retail SDK\\BuildTools** folder, run **msbuild /t:rebuild** on the root of the Retail SDK folder.</span></span> <span data-ttu-id="e5532-133">配置可能小売パッケージを生成するために、MSBuild ビルド ツールまたは Microsoft Visual Studio 開発者コマンド ライン ツールのいずれかを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e5532-133">You can use either the MSBuild build tool or the Microsoft Visual Studio developer command-line tool to generate the retail deployable packages.</span></span> <span data-ttu-id="e5532-134">パッケージを作成する前に、すべてのカスタマイズされたアセンブリを、**...\\Retail SDK\\References** フォルダに保存します。</span><span class="sxs-lookup"><span data-stu-id="e5532-134">Before you build the package, put all the customized assemblies in the **...\\Retail SDK\\References** folder.</span></span> <span data-ttu-id="e5532-135">さらに、**...\\Retail SDK\\Assets** フォルダーの **CommerceRuntime.Ext.config**、**CommerceRuntime.MPOSOffline.Ext.config**、 **HardwareStation.Extension.config**、および **RetailProxy.MPOSOffline.ext.config** のような変更済の構成ファイルを入力します。</span><span class="sxs-lookup"><span data-stu-id="e5532-135">Additionally, put the modified configuration files, such as **CommerceRuntime.Ext.config**, **CommerceRuntime.MPOSOffline.Ext.config**, **HardwareStation.Extension.config**, and **RetailProxy.MPOSOffline.ext.config**, in the **...\\Retail SDK\\Assets** folder.</span></span>

## <a name="retail-sdk-build-tools--customization-settings"></a><span data-ttu-id="e5532-136">Retail SDK ビルド ツール: カスタマイズ設定</span><span class="sxs-lookup"><span data-stu-id="e5532-136">Retail SDK build tools – Customization settings</span></span>
<span data-ttu-id="e5532-137">カスタマイズを構築しパッケージ化するために Retail SDK が使用するコンフィギュレーション値のほとんどが BuildTools\\Customization.setting files で設定されます。</span><span class="sxs-lookup"><span data-stu-id="e5532-137">Most of the configuration values that the Retail SDK uses to build and package customizations are set in the BuildTools\\Customization.setting files.</span></span> <span data-ttu-id="e5532-138">これらの値は、バイナリ、コンポーネント、パッケージの名前付け、バージョン管理、コード署名の方法を制御するメタデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="e5532-138">These values define metadata that controls how binaries, components, and packages are named, versioned, and code-signed.</span></span> <span data-ttu-id="e5532-139">このメタデータを定義した後、Retail SDK ビルド システムはカスタマイズ資産を識別し、すべての Retail コンポーネントのためにカスタマイズ資産をパッケージ化します。</span><span class="sxs-lookup"><span data-stu-id="e5532-139">After you define this metadata, the Retail SDK build system uses it to identify the customization assets and package them for all the Retail components.</span></span>

<span data-ttu-id="e5532-140">次のコンフィギュレーション設定は、 Customization.settings ファイルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="e5532-140">The following configuration settings are available in the Customization.settings file:</span></span>

- <span data-ttu-id="e5532-141">**AssemblyNamePrefix** - アセンブリの接頭語名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-141">**AssemblyNamePrefix** – Specify the prefix name for the assembly.</span></span> <span data-ttu-id="e5532-142">Retail SDK を作成するときは、すべてのアセンブリに接頭辞としてこの名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="e5532-142">When you build the Retail SDK, all the assemblies are prefixed with this name.</span></span>
- <span data-ttu-id="e5532-143">**CustomAssemblyVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム アセンブリ バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-143">**CustomAssemblyVersion** – Specify the custom assembly version for all assemblies that are built by using the Retail SDK.</span></span>
- <span data-ttu-id="e5532-144">**CustomVersion** - Retail SDK を使用して作成されたすべてのアセンブリのカスタム ファイル バージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-144">**CustomVersion** – Specify the custom file version for all assemblies that are built by using the Retail SDK.</span></span>
- <span data-ttu-id="e5532-145">**CustomName** - アセンブリのカスタム名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-145">**CustomName** – Specify the custom name for the assembly.</span></span>
- <span data-ttu-id="e5532-146">**CustomDescription** - アセンブリの説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-146">**CustomDescription** – Specify the description for the assembly.</span></span>
- <span data-ttu-id="e5532-147">**CustomPublisher** – アセンブリの発行元を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-147">**CustomPublisher** – Specify the publisher for the assembly.</span></span>
- <span data-ttu-id="e5532-148">**CustomPublisherDisplayName** - アセンブリの著作権を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-148">**CustomPublisherDisplayName** – Specify the copyright for the assembly.</span></span>
- <span data-ttu-id="e5532-149">**SignAssembly** – ビルド時にアセンブリに署名するには**はい**を指定してください。</span><span class="sxs-lookup"><span data-stu-id="e5532-149">**SignAssembly** – Specify **True** to sign the assembly during the build.</span></span>
- <span data-ttu-id="e5532-150">**DelaySign** – ビルド中にアセットの署名を延期するには **True** を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-150">**DelaySign** – Specify **True** to delay signing of the assets during the build.</span></span>
- <span data-ttu-id="e5532-151">**AssemblyOriginatorKeyFile** - アセンブリに署名するために使用する厳密な名前キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-151">**AssemblyOriginatorKeyFile** – Specify the strong name key to use to sign the assembly.</span></span>
- <span data-ttu-id="e5532-152">**ModernPOSPackageCertificateKeyFile** – Modern POS とハードウェア ステーションの署名に使用する個人情報交換 (PFX) ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-152">**ModernPOSPackageCertificateKeyFile** – Specify the Personal Information Exchange (PFX) file to use to sign Modern POS and Hardware station.</span></span>
- <span data-ttu-id="e5532-153">**RetailServerLibraryPathForProxyGeneration** – プロキシの生成に使用するカスタマイズされたRetail サーバー アセンブリを指定します (TypeScript と C\# プロキシの両方)。</span><span class="sxs-lookup"><span data-stu-id="e5532-153">**RetailServerLibraryPathForProxyGeneration** – Specify the customized Retail Server assembly to use for proxy generation (both TypeScript and C\# proxies).</span></span>

    <span data-ttu-id="e5532-154">7.1 以前のバージョンでは、ここで Retail サーバー アセンブリの名前を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5532-154">For 7.1 and earlier versions, you must specify the name of the Retail Server assembly here.</span></span>

    <span data-ttu-id="e5532-155">7.2 以降のバージョンでは、プロキシ生成の commerce ジェネレーター ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="e5532-155">For 7.2 and later versions, use the commerce generator tool for proxy generation.</span></span> <span data-ttu-id="e5532-156">ただし、E コマース クライアント側でプロキシを使用している場合は、ここでアセンブリ名を指定してください。</span><span class="sxs-lookup"><span data-stu-id="e5532-156">However, if you're using the proxy on the e-commerce client side, specify the assembly name here.</span></span>

- <span data-ttu-id="e5532-157">**ItemGroup** セクションには、次の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5532-157">The **ItemGroup** section includes the following settings:</span></span>

    - <span data-ttu-id="e5532-158">**ISV\_CommerceRuntime\_CustomizableFile** – すべてのカスタマイズされた CRT アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-158">**ISV\_CommerceRuntime\_CustomizableFile** – Specify the details of all the customized CRT assemblies.</span></span> <span data-ttu-id="e5532-159">各 CRT アセンブリに対して 1 つずつ、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e5532-159">You can have multiple entries, one for each CRT assembly.</span></span>

        <span data-ttu-id="e5532-160">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-160">**Example**</span></span>

        ```
        ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\MyCrtExtension.dll"
        ```

    - <span data-ttu-id="e5532-161">**ISV\_RetailServer\_CustomizableFile** – カスタマイズされたすべての Retail サーバー アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-161">**ISV\_RetailServer\_CustomizableFile** – Specify the details of all the customized Retail Server assemblies.</span></span> <span data-ttu-id="e5532-162">各 Retail サーバー アセンブリに対して 1 つの、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e5532-162">You can have multiple entries, one for each Retail Server assembly.</span></span>

        <span data-ttu-id="e5532-163">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-163">**Example**</span></span>

        ```
        ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\MyRetailServerExtension.dll"
        ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\MyRetailServerExtension2.dll"
        ```

    - <span data-ttu-id="e5532-164">**ISV\_RetailProxy\_CustomizableFile** – カスタマイズされたすべての Retail プロキシ アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-164">**ISV\_RetailProxy\_CustomizableFile** – Specify the details of all the customized Retail proxy assemblies.</span></span> <span data-ttu-id="e5532-165">各 Retail プロキシ アセンブリに対して 1 つの、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e5532-165">You can have multiple entries, one for each Retail proxy assembly.</span></span> 

        <span data-ttu-id="e5532-166">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-166">**Example**</span></span>

        ```
        ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\MyRetailProxyExtension.dll"
        ```

    - <span data-ttu-id="e5532-167">**ISV\_HardwareStation\_CustomizableFile** – カスタマイズされたすべてのハードウェア ステーション アセンブリの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-167">**ISV\_HardwareStation\_CustomizableFile** – Specify the details of all the customized Hardware station assemblies.</span></span> <span data-ttu-id="e5532-168">カスタマイズされた各ハードウェア ステーション アセンブリに対して 1 つずつ、複数のエントリを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e5532-168">You can have multiple entries, one for each customized Hardware station assembly.</span></span>

        <span data-ttu-id="e5532-169">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-169">**Example**</span></span>

        ```
        ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\MyHardwareStationExtension.dll"
        ```

    - <span data-ttu-id="e5532-170">**ISV\_CustomDatabaseFile\_アップグレード\_カスタム** – カスタマイズされたすべてのデータベース スクリプトの詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5532-170">**ISV\_CustomDatabaseFile\_Upgrade\_Custom** – Specify the details of all the customized database scripts.</span></span>

        <span data-ttu-id="e5532-171">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-171">**Example**</span></span>

        ```
        ISV_CustomDatabaseFile_Upgrade_Custom Include="$(SdkRootPath)\Database\Upgrade\Custom\SqlUpdatev1.sql"
        ```

> [!IMPORTANT]
> <span data-ttu-id="e5532-172">ビルド プロセスを開始する前に、拡張アセンブリを \\Retail SDK\\References に、カスタム データベース スクリプトを \\RetailSDK\\Database\Upgrade\\Custom に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5532-172">Before you start the build process, you must put extension assemblies in ...\\Retail SDK\\References and custom database scripts under ...\\RetailSDK\\Database\Upgrade\\Custom.</span></span>

### <a name="database-scripts"></a><span data-ttu-id="e5532-173">データベース スクリプト</span><span class="sxs-lookup"><span data-stu-id="e5532-173">Database scripts</span></span>
<span data-ttu-id="e5532-174">データベース スクリプトは、Retail サーバーおよび Modern POS オフライン パッケージとともにパッケージ化され、Retail Server および Modern POS がインストールされたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="e5532-174">Database scripts are packaged together with the Retail Server and Modern POS Offline packages, and are run when Retail Server and Modern POS are installed.</span></span> <span data-ttu-id="e5532-175">複数のカスタム データベース スクリプトがある場合は、アルファベット順に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e5532-175">If there are multiple custom database scripts, they are run in alphabetical order.</span></span> <span data-ttu-id="e5532-176">したがって、スクリプトを特定の順序で実行したい場合は、それに応じて名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5532-176">Therefore, to run the scripts in a specific order, you must name them accordingly.</span></span> <span data-ttu-id="e5532-177">CRT.RETAILUPGRADEHISTORY テーブルは、データベースに既に適用されているスクリプトを追跡します。</span><span class="sxs-lookup"><span data-stu-id="e5532-177">The CRT.RETAILUPGRADEHISTORY table tracks the scripts that are already applied to the database.</span></span> <span data-ttu-id="e5532-178">したがって、次のパッケージ アップグレードは、CRT.RETAILUPGRADEHISTORY テーブルに項目がないアップグレード スクリプトのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="e5532-178">Therefore, the next package upgrade runs only the upgrade scripts that don't have an entry in the CRT.RETAILUPGRADEHISTORY table.</span></span>

## <a name="update-the-extension-configuration-files"></a><span data-ttu-id="e5532-179">拡張機能の構成ファイルを更新します</span><span class="sxs-lookup"><span data-stu-id="e5532-179">Update the extension configuration files</span></span>
<span data-ttu-id="e5532-180">CRT、Retail Server、ハードウェア ステーション、またはプロキシに新しい拡張機能がある場合は、関連する拡張構成ファイルの\<構成\>セクションに拡張アセンブリの詳細を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5532-180">If you have any new extensions in CRT, Retail Server, Hardware station, or proxy, you should register the details of the extension assemblies in the \<composition\> section of the relevant extension configuration file.</span></span> <span data-ttu-id="e5532-181">すべての拡張設定ファイルは次で見つけることができます。\\RetailSDK\\資産フォルダ。</span><span class="sxs-lookup"><span data-stu-id="e5532-181">You can find all the extension configuration files in the ...\\RetailSDK\\Assets folder.</span></span> <span data-ttu-id="e5532-182">すべての拡張機能は拡張ファイルの情報に基づいて読み込まれるため、アセンブリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5532-182">Because all extensions are loaded based on the information in the extension configuration files, you must register your assemblies there.</span></span>

<span data-ttu-id="e5532-183">パッケージを行う前に、次の構成ファイルを更新する必要があります (この領域でカスタマイズがある場合)。</span><span class="sxs-lookup"><span data-stu-id="e5532-183">Before you do the package, you must update the following configuration files if you have any customization in that area:</span></span>

- <span data-ttu-id="e5532-184">**CommerceRuntime.Ext.config** – すべての CRT 拡張アセンブリを登録します。</span><span class="sxs-lookup"><span data-stu-id="e5532-184">**CommerceRuntime.Ext.config** – Register all your CRT extension assemblies.</span></span>

    <span data-ttu-id="e5532-185">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-185">**Example**</span></span>

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <!-- Register your own assemblies here. -->
            <add source="assembly" value="my custom library" />
        </composition>
    </commerceRuntimeExtensions>
    ```

- <span data-ttu-id="e5532-186">**CommerceRuntime.MPOSOffline.Ext.config** – オフラインで、すべての CRT 拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="e5532-186">**CommerceRuntime.MPOSOffline.Ext.config** – Register all your CRT extensions for offline.</span></span>

    <span data-ttu-id="e5532-187">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-187">**Example**</span></span>

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <!-- Register your own assemblies or types here. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </commerceRuntimeExtensions>
    ```

- <span data-ttu-id="e5532-188">**HardwareStation.Extension.config** – すべてのハードウェア ステーション拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="e5532-188">**HardwareStation.Extension.config** – Register all your Hardware station extensions.</span></span>

    <span data-ttu-id="e5532-189">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-189">**Example**</span></span>

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <hardwareStationExtension>
        <composition>
            <! -- Register your own assemblies or types here. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </hardwareStationExtension>
    ```

- <span data-ttu-id="e5532-190">**RetailProxy.MPOSOffline.ext.config** – すべての小売プロキシ拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="e5532-190">**RetailProxy.MPOSOffline.ext.config** – Register all your retail proxy extensions.</span></span>

    <span data-ttu-id="e5532-191">**例**</span><span class="sxs-lookup"><span data-stu-id="e5532-191">**Example**</span></span>

    ```C#
    <?xml version="1.0" encoding="utf-8"?>
    <retailProxyExtensions>
        <composition>
            <!-- Register your own proxy extension assemblies. -->
            <add source="assembly" value=" my custom library" />
        </composition>
    </retailProxyExtensions>
    ```

### <a name="retail-server-extension-assemblies"></a><span data-ttu-id="e5532-192">Retail サーバーの拡張機能アセンブリ</span><span class="sxs-lookup"><span data-stu-id="e5532-192">Retail Server extension assemblies</span></span>
<span data-ttu-id="e5532-193">パッケージを開始する前に、Retail Server web.config file の \<extensionComposition\> に、Retail Server 拡張アセンブリのエントリを追加する必要があります。これにより、アセンブリがロードされ、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e5532-193">Before you start the package, you must add an entry for the Retail Server extension assemblies in the \<extensionComposition\> of the Retail Server web.config file, so that the assemblies are loaded and used.</span></span> <span data-ttu-id="e5532-194">web.config ファイルは、Retail SDK\\パッケージ\\RetailServer\\ コード フォルダーで検索できます。</span><span class="sxs-lookup"><span data-stu-id="e5532-194">You can find the web.config file in the Retail SDK\\Packages\\RetailServer\\Code folder.</span></span>

<span data-ttu-id="e5532-195">次の図は、Retail サーバーの Web.config ファイルの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e5532-195">The following illustration shows an example of a Retail Server web.config file.</span></span>

<span data-ttu-id="e5532-196">[![Retail サーバーの Web.config ファイル](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)</span><span class="sxs-lookup"><span data-stu-id="e5532-196">[![Retail Server web.config file](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)</span></span>

## <a name="generate-a-retail-deployable-package"></a><span data-ttu-id="e5532-197">配置可能小売パッケージを生成</span><span class="sxs-lookup"><span data-stu-id="e5532-197">Generate a retail deployable package</span></span>
<span data-ttu-id="e5532-198">配置可能小売パッケージを生成するには、MSBuild ビルド コマンド プロンプト ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5532-198">To generate the retail deployable package, open the MSBuild build Command Prompt window.</span></span> <span data-ttu-id="e5532-199">(開発者仮想マシンの、**開始**メニューで **msbuild** を検索します。) そして、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e5532-199">(On the developer virtual machine, search for **msbuild** on the **Start** menu.) Then run the following command.</span></span>

```
msbuild /p:Configuration=Release
```

<span data-ttu-id="e5532-200">Microsoft Visual Studio 2015 開発者コマンド ライン ツールで同じコマンドを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="e5532-200">You can also run the same command in the Microsoft Visual Studio 2015 developer command-line tool.</span></span>

### <a name="packages"></a><span data-ttu-id="e5532-201">パッケージ</span><span class="sxs-lookup"><span data-stu-id="e5532-201">Packages</span></span>
<span data-ttu-id="e5532-202">ビルドが完了した後、Retail SDK\\Packages\\RetailDeployablePackage フォルダーに、配置可能小売パッケージ が zip ファイルとして (RetailDeployablePackage.zip) が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e5532-202">After the build is completed, retail deployable packages are generated as a zip file (RetailDeployablePackage.zip) in the Retail SDK\\Packages\\RetailDeployablePackage folder.</span></span>

> [!NOTE]
> <span data-ttu-id="e5532-203">さまざまな Retail コンポーネントを別々のパッケージにすることはありません。</span><span class="sxs-lookup"><span data-stu-id="e5532-203">There won't be separate packages the various Retail components.</span></span> <span data-ttu-id="e5532-204">すべてのパッケージは、RetailDeployablePackage という名の 1 つのバンドル パッケージに結合されます。</span><span class="sxs-lookup"><span data-stu-id="e5532-204">All the packages will be combined into one bundle package that is named RetailDeployablePackage.</span></span>

## <a name="deploy-the-retail-deployable-packages"></a><span data-ttu-id="e5532-205">小売展開可能パッケージを配置する</span><span class="sxs-lookup"><span data-stu-id="e5532-205">Deploy the retail deployable packages</span></span>
<span data-ttu-id="e5532-206">手動または LCS 自動化フローを使用してパッケージを配置する方法については、[配置可能なパッケージを適用する](../../../dev-itpro/deployment/apply-deployable-package-system.md)および[配置可能なパッケージをインストールする](../../../dev-itpro/deployment/install-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5532-206">For information about how to deploy the packages either manually or by using the automated flow in LCS, see [Apply a deployable package](../../../dev-itpro/deployment/apply-deployable-package-system.md) and [Install a deployable package](../../../dev-itpro/deployment/install-deployable-package.md).</span></span>

